<!-- hide -->
# Create a Blog from Scratch with Next.js and Markdown
<!-- endhide -->

<onlyfor saas="false" withBanner="false">

## 🌱 How to start this project?

This project does not have a 4Geeks starter repository. Instead, follow the [official Next.js documentation](https://nextjs.org/docs/getting-started) to create a basic repository.

We recommend starting the project using [Codespaces](https://4geeks.com/lesson/what-is-github-codespaces) (recommended) or [Gitpod](https://4geeks.com/lesson/how-to-use-gitpod). Alternatively, you can work locally if you have Node.js installed.

> ⚠ Make sure to install the necessary dependencies when starting your project with `npm install`.

</onlyfor>

## 📝 Instructions

### Step 1: Set Up the Blog Foundation

- [ ] Follow the guide from the official Next.js documentation to create a basic project.  

- [ ] Create a new project with the command:  

```bash
npx create-next-app@latest blog
```

### Step 2: Basic Blog Structure

- [ ] Create a `posts/` folder in the root directory to store the Markdown files (`.md` or `.mdx`) that will contain your blog content.  

- [ ] Add example Markdown files with data such as the title, date, and content of the post.  

### Step 3: Generate Blog Content with AI

- [ ] Use a tool like ChatGPT to generate engaging content for your blog posts.  

- [ ] You can request catchy titles, interesting introductions, or even a full article using specific prompts.  

### Step 4: Render Blog Content

- [ ] Configure Next.js to read the Markdown files from the `posts/` folder and display them on your blog.  

- [ ] Use functions like `getStaticProps` or `getStaticPaths` to render posts statically.  

Example to read Markdown files (you should have a function similar to this):  

```javascript
import fs from 'fs';
import path from 'path';
import matter from 'gray-matter';

export async function getStaticProps() {
  const filePath = path.join(process.cwd(), 'posts', 'example.md');
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

### Step 5: Design and Improve the Interface

- [ ] Use CSS or a library like TailwindCSS to style your blog.  

- [ ] Design a homepage that lists all posts with a summary and a "read more" link.  

- [ ] Improve the individual post pages to make them visually appealing and easy to read.  

### Step 6: Advanced Features (Optional)

- [ ] **Categories and Tags**: Add functionality to filter posts by category or tags.  

- [ ] **Search Bar**: Implement a search bar to help users find specific content.  

- [ ] **Dark Mode**: Add a button to toggle between light and dark mode.  

- [ ] **Comments**: Integrate a solution like Disqus to allow comments on posts.  

- [ ] **SEO Optimization**: Ensure each page has unique metadata and descriptions to improve search engine visibility.  

### Bonus: Publish Your Blog  

- [ ] Deploy your blog using [Vercel](https://vercel.com/), a perfect platform for Next.js projects.  

Explore different ways to enhance your blog to make it more complete and functional.