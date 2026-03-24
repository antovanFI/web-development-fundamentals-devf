# 🎓 Portal de Ingeniería - Materiales de Clase

Este proyecto es un portal web educativo responsivo, diseñado para centralizar y distribuir materiales de clase, recursos técnicos y herramientas para estudiantes de ingeniería. 

El sitio está optimizado para garantizar una lectura cómoda y una navegación fluida desde cualquier dispositivo (celulares, tablets y computadoras de escritorio).

## 🚀 Arquitectura del Proyecto y Tecnologías

El desarrollo de esta interfaz gráfica (Frontend) se realizó aplicando las mejores prácticas de maquetación moderna, sin el uso de frameworks externos, basándose puramente en **HTML5 Semántico** y **CSS3**.

### Estrategia de Diseño: Mobile-First
El código CSS fue estructurado comenzando por la vista móvil (la más restrictiva en espacio) y escalando progresivamente mediante el uso de **Media Queries**. Se definieron dos *breakpoints* principales:
- `>= 768px` (Tablets): Transición de estructuras apiladas a cuadrículas de 2 columnas.
- `>= 1024px` (Desktop): Expansión a 3 columnas y reubicación del panel de herramientas como barra lateral fija (`sticky`).

### Sistemas de Layout (CSS)
Para la distribución espacial de los elementos, se implementó una combinación estratégica de los dos modelos de maquetación nativos de CSS:

1. **Flexbox (Unidimensional):** - Utilizado para la barra de navegación (`header.navbar`), alineando el logotipo y los enlaces mediante `justify-content: space-between` y `align-items: center`.
   - Implementado en el contenedor principal (`.layout-principal`) para manejar la transición de eje vertical (`flex-direction: column`) en móviles, a eje horizontal (`flex-direction: row`) en pantallas grandes, distribuyendo el espacio con proporciones dinámicas (`flex: 3` vs `flex: 1`).

2. **CSS Grid (Bidimensional):**
   - Utilizado exclusivamente para el catálogo de recursos (`.recursos-grid`).
   - Permite una cuadrícula rígida y escalable mediante `grid-template-columns: repeat(auto-fit, minmax(300px, 1fr))`, garantizando que las tarjetas de las asignaturas mantengan su simetría independientemente de la resolución de la pantalla.

3. **Variables CSS (Custom Properties):**
   - Centralización de la paleta de colores y variables de interfaz en la pseudo-clase `:root` para facilitar la escalabilidad y futuros modos oscuros (Dark Mode).

## 📚 Contenido del Portal

El portal organiza recursos clave para el desarrollo de software y administración de sistemas:
- **Administración de Servidores:** Comandos esenciales y avanzados en terminales Linux.
- **Modelado de Datos:** Diseño de bases de datos relacionales y diagramas Entidad-Relación (notación Chen).
- **Cloud Computing:** Arquitectura de software y despliegue de aplicaciones en la nube utilizando Microsoft Azure.
- **Programación Lógica:** Configuración de entornos y resolución de algoritmos mediante Prolog.

## ⚙️ Despliegue (Deployment)

El proyecto está preparado para ser alojado de forma estática y gratuita a través de **GitHub Pages**. 
Cualquier actualización en la rama `main` de este repositorio se reflejará automáticamente en la URL pública del sitio.

---
*Desarrollado como proyecto de maquetación web y portal de apoyo docente.*
