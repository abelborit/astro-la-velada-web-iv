# Notas:

- Para usar una fuente en específico se pueden usar algunos herramientas como:
  - https://fontsource.org/
  - https://fonts.google.com/

  - Fontsource (self-hosting) and Google Fonts differ mainly in performance and privacy. Fontsource allows you to bundle fonts directly into your project via npm, offering better speed, offline functionality, privacy, and version control. Google Fonts uses a CDN to serve fonts, which is easy to set up, offers massive variety, and potentially faster loading for users who have cached them from other sites. (https://stackoverflow.com/questions/35065185/server-stored-fonts-vs-google-fonts#:~:text=There%20are%20some%20advantages%20to%20storing%20fonts,device%20is%20being%20used%20to%20access%20it)

  ```
  @font-face {
    font-family: "Jost Variable";
    src:
      url("/fonts/jost-variable/webfonts/jost-cyrillic-800-normal.woff2")
        format("woff2"),
      /* woff/woff2 -> Formato optimizado para la web, recomendado y soportado por todos los navegadores modernos. (formato web como principal) */
        url("/fonts/jost-variable/ttf/jost-cyrillic-800-normal.ttf")
        format("truetype"); /* Formato más antiguo, útil como fallback para navegadores antiguos. (formato tradicional como respaldo) */
    font-weight: normal;
    font-style: normal;
    font-display: swap; /* El texto se muestra inmediatamente con una fuente de respaldo (fallback) y, cuando la fuente personalizada termina de cargar, se reemplaza automáticamente. Es la opción más recomendada para buena experiencia de usuario. */
  }
  ```

---

# Astro Starter Kit: Basics

```sh
npm create astro@latest -- --template basics
```

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
│   └── favicon.svg
├── src
│   ├── assets
│   │   └── astro.svg
│   ├── components
│   │   └── Welcome.astro
│   ├── layouts
│   │   └── Layout.astro
│   └── pages
│       └── index.astro
└── package.json
```

To learn more about the folder structure of an Astro project, refer to [our guide on project structure](https://docs.astro.build/en/basics/project-structure/).

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).
