<!-- hide -->
# Crea un Blog desde Cero con Next.js y Markdown
<!-- endhide -->

<onlyfor saas="false" withBanner="false">

## 🌱 ¿Cómo iniciar este proyecto?

Este proyecto no cuenta con un repositorio base de 4Geeks. En su lugar, sigue la [documentación oficial de Next.js](https://nextjs.org/docs/getting-started) para crear un repositorio básico.

Te recomendamos abrir el proyecto usando [Codespaces](https://4geeks.com/lesson/what-is-github-codespaces) (recomendado) o [Gitpod](https://4geeks.com/lesson/how-to-use-gitpod). Alternativamente, puedes trabajar localmente si tienes Node.js instalado.

> ⚠ Asegúrate de instalar las dependencias necesarias al iniciar tu proyecto con `npm install`.

</onlyfor>

## 📝 Instrucciones

### Paso 1: Configura la Base del Blog

- [ ] Sigue la guía de la documentación oficial de Next.js para crear un proyecto básico.  

- [ ] Crea un nuevo proyecto con el comando:  

```bash
npx create-next-app@latest blog
```

### Paso 2: Estructura Básica del Blog

- [ ] Crea una carpeta `posts/` en el directorio raíz para almacenar los archivos Markdown (`.md` o `.mdx`) que contendrán el contenido de tus publicaciones.  

- [ ] Añade ejemplos de archivos Markdown con datos como el título, la fecha y el contenido del post.  

### Paso 3: Genera Contenido para el Blog con IA

- [ ] Usa una herramienta como ChatGPT para generar contenido atractivo para las publicaciones de tu blog.  

- [ ] Puedes pedir títulos llamativos, introducciones interesantes o incluso generar un artículo completo con prompts específicos.  

### Paso 4: Renderiza el Contenido en el Blog

- [ ] Configura Next.js para leer los archivos Markdown de la carpeta `posts/` y mostrarlos en tu blog.  

- [ ] Usa funciones como `getStaticProps` o `getStaticPaths` para renderizar las publicaciones de manera estática.  

Ejemplo para leer archivos Markdown debes tener una función similar a esta:  

```javascript
import fs from 'fs';
import path from 'path';
import matter from 'gray-matter';

export async function getStaticProps() {
  const filePath = path.join(process.cwd(), 'posts', 'ejemplo.md');
  const fileContent = fs.readFileSync(filePath, 'utf8');
  const { data, content } = matter(fileContent);

  return {
    props: {
      data,
      content,
    },
  };
}
```

### Paso 5: Diseña y Mejora la Interfaz

- [ ] Usa CSS o una librería como TailwindCSS para darle estilo a tu blog.  

- [ ] Diseña una página principal que liste todas las publicaciones con un resumen y un enlace para "leer más".  

- [ ] Mejora las páginas individuales de cada publicación para que sean visualmente atractivas y fáciles de leer.  

### Paso 6: Funcionalidades Avanzadas (Opcional)

- [ ] **Categorías y Etiquetas**: Añade funcionalidad para filtrar publicaciones por categoría o etiquetas.  

- [ ] **Buscador**: Implementa una barra de búsqueda para facilitar a los usuarios encontrar contenido específico.  

- [ ] **Modo Oscuro**: Agrega un botón para alternar entre modo claro y oscuro.  

- [ ] **Comentarios**: Integra una solución como Disqus para permitir comentarios en las publicaciones.  

- [ ] **Optimización SEO**: Asegúrate de que cada página tenga metadatos y descripciones únicas para mejorar la visibilidad en motores de búsqueda.  

### Bonus: Publica tu Blog  

- [ ] Despliega tu blog usando [Vercel](https://vercel.com/), una plataforma ideal para proyectos con Next.js.  

Explora diferentes formas de mejorar tu blog para que sea más completo y funcional.