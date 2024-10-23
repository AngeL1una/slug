# slug - Angel Luna Lugo -MoonDev
# Proyecto de Desarrollo Web

## URLs Amigables (Slugs)

En el desarrollo web, un **slug** es la parte de una URL que identifica de manera única una página de un sitio web de una manera legible para los usuarios y optimizada para motores de búsqueda (SEO). Los slugs suelen ser descriptivos, claros y se utilizan para mejorar la estructura de las URLs.

### Ejemplo de Slug

Supongamos que tenemos un sitio de comercio electrónico que vende productos como AirPods. Una URL amigable para la página de un producto específico podría verse así:

https://www.ejemplo.com/productos/Apple-AirPods-generacion-Estuche-MagSafe


En esta URL:
- **Dominio**: `https://www.ejemplo.com/`
- **Ruta**: `productos`
- **Slug**: `Apple-AirPods-generacion-Estuche-MagSafe`

El **slug** en este caso es `Apple-AirPods-generacion-Estuche-MagSafe`, y describe de manera clara el contenido de la página. Esto ayuda a que la URL sea más fácil de entender y mejora la visibilidad del sitio en los motores de búsqueda.

### Beneficios de Usar Slugs

1. **Mejora la experiencia del usuario**: URLs más limpias y entendibles.
2. **Optimización para SEO**: Aumenta la probabilidad de que la página aparezca en resultados de búsqueda relevantes.
3. **Facilita el acceso**: Los usuarios pueden recordar la URL con mayor facilidad.

### Cómo Implementar Slugs

En el backend, el slug se suele generar a partir del título de la página o del nombre del producto. Aquí te dejo un ejemplo en JavaScript para generar un slug a partir de una cadena de texto:

```javascript
function generarSlug(texto) {
    return texto
        .toLowerCase()                  // Convierte el texto a minúsculas
        .replace(/ /g, '-')             // Reemplaza espacios con guiones
        .replace(/[^\w-]+/g, '');       // Elimina caracteres no alfanuméricos
}

const titulo = "Apple AirPods generación Estuche MagSafe";
const slug = generarSlug(titulo);

console.log(slug);  // Salida: "apple-airpods-generacion-estuche-magsafe"
