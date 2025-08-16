# 📊 Censo 2018 — El Progreso

Proyecto web en **HTML5 + Bootstrap 5 + JavaScript** que consume la API del **Censo 2018 de Guatemala** para mostrar los indicadores de los municipios del departamento de **El Progreso**.  

## 🚀 Funcionalidades

- Selección de municipio (códigos 201–208)  
- Consulta a la **API oficial** de indicadores:  
  ```
  https://censopoblacion.azurewebsites.net/API/indicadores/2/{codigo}
  ```
- Visualización de datos en **tablas dinámicas** con **barras de progreso**:
  - 📌 Indicadores generales  
  - 📚 Educación  
  - 🏠 Vivienda y hogares  
  - 👥 Población por sexo  
  - 🌆 Población por área (urbana/rural)  
  - 🎂 Población por grandes grupos de edad  
  - 🧑🏽‍🤝‍🧑🏻 Población por pueblos  
- **Comparativas**:
  - Totales de población por municipio  
  - Indicadores clave (educación, hogares, edad, etc.)  
- Exportación a **CSV** de las tablas comparativas  
- Cache en **LocalStorage** para no repetir consultas  
- Layout con **header fijo** y **footer fijo negro**  

## ⚙️ Tecnologías utilizadas

- **HTML5** — estructura semántica  
- **Bootstrap 5.3** — estilos base y componentes responsivos  
- **Bootstrap Icons** — iconografía ligera  
- **CSS personalizado** (`styles.css`) — para el diseño moderno y limpio  
- **JavaScript puro** — consumo de API, render dinámico, caché y exportación CSV  

---

## 📂 Estructura del proyecto

```
censo-el-progreso/
│── index.html        # Página principal (estructura HTML y lógica JS)
│── styles.css        # Estilos personalizados
│── README.md         # Documentación
```

---

## ▶️ Cómo usar

1. Clonar o descargar este repositorio.
2. Abrir `index.html` en un navegador con **Live Server** o un hosting simple (ej. GitHub Pages).  
   ⚠️ Si lo abres solo con `file://`, algunas funciones de **fetch (API)** pueden bloquearse por CORS.  
3. Selecciona un municipio en el menú desplegable y presiona **“Cargar datos”**.  
4. Explora los paneles con indicadores y usa los botones de **comparativa** para ver todos los municipios juntos.  

---

## 📊 Ejemplo de API

### Endpoint
```
https://censopoblacion.azurewebsites.net/API/indicadores/2/205
```

### Respuesta (El Jícaro)
```json
{
  "id": 25,
  "depto_id": 2,
  "municipio_id": 205,
  "nombre": "El Jícaro",
  "pob_total": 13128,
  "indice_masculinidad": 97.29,
  "prom_hijos_mujer": 3.58,
  "edad_promedio": 29.63,
  "indice_dependencia": 56.83,
  "anios_prom_estudio": 6.52,
  "alfabetismo": 86.14,
  "viviendas_part": 4217,
  "total_hogares": 3456,
  "prom_personas_hogar": 3.8,
  "total_jefas_hogar": 25.81,
  "...": "otros campos"
}
```

---


**Milton Joetd Gómez Marroquín**  
`1890-22-10379`
