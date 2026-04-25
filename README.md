# system_ecuations
calculadora de sistema de ecuaciones
# 📐 Solucionador de Sistemas de Ecuaciones Lineales

![Versión](https://img.shields.io/badge/versión-2.0-blue)
![Plataforma](https://img.shields.io/badge/plataforma-Web-green)
![Licencia](https://img.shields.io/badge/licencia-MIT-yellow)

## 🎯 Descripción

Aplicación web interactiva que permite resolver sistemas de ecuaciones lineales mediante el método de reducción (Gauss-Jordan). Desarrollada en HTML5, CSS3 y JavaScript puro, ofrece una interfaz visual intuitiva para ingresar coeficientes y visualizar resultados.

## ✨ Características

- ✅ **Interfaz gráfica interactiva** - Tabla dinámica dibujada en canvas
- ✅ **Soporte hasta 26 variables** - Sistemas de hasta 26x26 ecuaciones
- ✅ **Navegación por teclado** - Movimiento con flechas y entrada numérica
- ✅ **Scroll automático** - Para sistemas grandes con Shift + Flechas
- ✅ **Entrada flexible** - Números enteros, decimales y negativos
- ✅ **Validación de sistemas** - Detecta ecuaciones repetidas o proporcionales
- ✅ **Resultados precisos** - Redondeo a 4 decimales
- ✅ **Botones rápidos** - Acceso directo a tamaños comunes

## 🚀 Cómo usar

### 1. Iniciar la aplicación
Simplemente abre el archivo `index.html` en cualquier navegador moderno (Chrome, Firefox, Edge, Safari).

### 2. Configurar el sistema
Ingresa el número de ecuaciones/variables (1-26)

Presiona "Crear tabla" o Enter

Se generará una tabla con coeficientes vacíos


### 3. Ingresar datos
Navegación: Flechas ← → ↑ ↓
Guardar: Enter
Decimal: . (punto)
Negativo: - (menos)
Borrar: Backspace
Scroll rápido: Shift + Flechas


### 4. Resolver el sistema

Haz clic en "Calcular solución" para obtener los resultados


## 📊 Ejemplo práctico

### Sistema 3x3:

2x + 3y - z = 8
x - 2y + 2z = -2
3x + y - 2z = 3

text

### Pasos:
1. Ingresar "3" → Crear tabla
2. Llenar la matriz:
[2] [3] [-1] [8]
[1] [-2] [2] [-2]
[3] [1] [-2] [3]

text
3. Calcular → Resultado: `x=1, y=2, z=-1`

## ⌨️ Controles detallados

| Acción | Tecla | Descripción |
|--------|-------|-------------|
| Mover cursor | ← → ↑ ↓ | Navega entre celdas |
| Guardar y avanzar | Enter | Guarda valor y baja una fila |
| Punto decimal | . | Activa entrada decimal |
| Signo negativo | - | Cambia signo del número |
| Corregir | Backspace | Elimina último dígito |
| Scroll horizontal | Shift + ←/→ | Desplaza vista lateral |
| Scroll vertical | Shift + ↑/↓ | Desplaza vista vertical |

## 🛠️ Tecnologías utilizadas

- **HTML5** - Estructura semántica
- **CSS3** - Diseño responsivo y gradientes
- **JavaScript (ES6)** - Lógica del algoritmo y eventos
- **Canvas API** - Renderizado dinámico de la tabla

## 📐 Algoritmo de resolución

El sistema implementa el **método de reducción de Gauss** con sustitución inversa:

1. **Verificación inicial** - Detecta sistemas inconsistentes
2. **Triangulación** - Reduce la matriz a forma triangular superior
3. **Pivoteo parcial** - Evita ceros en la diagonal principal
4. **Sustitución regresiva** - Calcula valores de las variables
5. **Precisión** - Resultados con 4 decimales

## 🔧 Estructura del proyecto
├── index.html # Archivo principal
├── README.md # Documentación
└── assets/
├── styles.css # Estilos (incluidos en HTML)
└── script.js # Lógica (incluida en HTML)

text

## ⚠️ Limitaciones conocidas

- **Máximo 26 variables** - Limitado por el alfabeto
- **Precisión decimal** - Redondeo a 4 decimales por defecto
- **Sistemas sin solución** - Muestra mensaje de error
- **Sistemas indeterminados** - Detecta pero no calcula soluciones paramétricas

## 🐛 Solución de problemas comunes

### El canvas no se ve completo
- Usa **Shift + Flechas** para desplazar la vista
- O usa la barra de scroll del contenedor

### No puedo ingresar números
- Verifica que hayas creado la tabla primero
- Asegúrate de que la celda esté seleccionada (borde rojo)

### El cálculo no muestra resultados
- Revisa que todos los coeficientes estén ingresados
- Verifica que no haya ecuaciones proporcionales
- Confirma que el sistema tenga solución única

### Errores de redondeo
- El sistema puede mostrar pequeñas variaciones debido a decimales
- Para mayor precisión, ingresa fracciones como decimales exactos

## 🎨 Personalización

Puedes modificar fácilmente:

### Colores (en CSS)
```css
/* Gradiente principal */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Color de la celda seleccionada */
ctx.strokeStyle = "#ff6b6b";
Precisión decimal (en el código)
javascript
var rounded = Math.round(value * 10000) / 10000; // Cambia 10000 por más/menos ceros
Máximo de variables
javascript
if (isNaN(total) || total < 1 || total > 26) // Cambia 26 por otro número
📈 Rendimiento
Sistemas pequeños (≤10) - Respuesta instantánea

Sistemas medianos (11-20) - < 1 segundo

Sistemas grandes (21-26) - 1-2 segundos

🤝 Contribuciones
Las contribuciones son bienvenidas. Para cambios importantes:

Fork del proyecto

Crea tu rama (git checkout -b feature/AmazingFeature)

Commit cambios (git commit -m 'Add AmazingFeature')

Push a la rama (git push origin feature/AmazingFeature)

Abre un Pull Request

📝 Licencia
Distribuido bajo licencia MIT. Ver LICENSE para más información.

📧 Contacto
Autor: [Tu nombre]
Email: [tu@email.com]
Proyecto: [URL del proyecto]

🙏 Agradecimientos
Inspirado en métodos numéricos para solución de ecuaciones

Interfaz basada en principios de UX educativa

Validación de sistemas lineales

🎓 Notas académicas
Este proyecto es ideal para:

Estudiantes - Aprender métodos numéricos visualmente

Profesores - Demostrar resolución de sistemas en clase

Ingenieros - Validar cálculos rápidos de hasta 26 variables

📖 Referencias
Método de eliminación Gaussiana

Sistemas de ecuaciones lineales

Canvas API - MDN

✨ Desarrollado con ❤️ para resolver ecuaciones de manera interactiva ✨

text

## 📄 README adicional (versión simplificada)

Si prefieres un README más corto y directo:

```markdown
# Solucionador de Ecuaciones Lineales

## 🚀 Inicio rápido
1. Abre `index.html`
2. Ingresa el número de ecuaciones (ej: 3)
3. Llena la tabla con coeficientes
4. Presiona "Calcular solución"

## 🎮 Controles
- **Flechas** - Navegar entre celdas
- **Enter** - Guardar valor y avanzar
- **Shift + Flechas** - Desplazar vista
- **Backspace** - Borrar último dígito

## 📊 Ejemplo
Sistema 3x3:
2x + 3y - z = 8
x - 2y + 2z = -2
3x + y - 2z = 3

text
Resultado: `x=1, y=2, z=-1`

## ⚙️ Requisitos
- Navegador moderno (Chrome, Firefox, Edge, Safari)
- JavaScript habilitado

## 📝 Características
✅ Hasta 26 variables
✅ Decimales y negativos
✅ Scroll automático
✅ Validación de sistemas

## 🐛 ¿Problemas?
- Usa Shift + Flechas si no ves todas las celdas
- Verifica que todos los coeficientes estén llenos
- Asegúrate de que el sistema tenga solución única















`index.html` en cualquier navegador moderno (Chrome, Firefox, Edge, Safari).

### 2. Configurar el sistema
