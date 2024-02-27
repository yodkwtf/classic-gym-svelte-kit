## Creating a New Svelte App

1. Create a new Svelte app

   ```bash
   npm create svelte@latest my-svelte-app
   ```

2. Select the options you want and then navigate to the new directory

   ```bash
   cd my-svelte-app
   ```

3. Open the project in your code editor

   ```bash
   code .
   ```

4. Start the development server

   ```bash
   npm run dev
   ```

5. Open your browser and navigate to `localhost:5175`

## Setting Up Tailwind CSS

1. Install Tailwind CSS

   ```bash
   npm install -D tailwindcss postcss autoprefixer
   ```

2. Create a `tailwind.config.js` file

   ```bash
   npx tailwindcss init -p
   ```

3. Enable use of PostCSS in style blocks

   ###### svelte.config.js

   ```js
   import adapter from '@sveltejs/adapter-auto';
   import { vitePreprocess } from '@sveltejs/vite-plugin-svelte';
   /** @type {import('@sveltejs/kit').Config} */
   const config = {
     kit: {
       adapter: adapter(),
     },
     preprocess: vitePreprocess(),
   };
   export default config;
   ```

4. Configure your template paths

   ###### tailwind.config.js

   ```js
   /** @type {import('tailwindcss').Config} */
   export default {
     content: ['./src/**/*.{html,js,svelte,ts}'],
     theme: {
       extend: {},
     },
     plugins: [],
   };
   ```

5. Add the Tailwind directives to your CSS

   ###### ./src/app.css

   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

6. Import your CSS file into your Svelte components

   ###### ./src/routes/+layout.svelte

   ```js
   <script>
    import "../app.css";
   </script>

   <slot />
   ```

## Project Folder Structure

The SvelteKit project structure is as follows:

#### ./src

- the main source folder
- contains the routes, components, and assets
- the entry point for the application is `./src/routes/+page.svelte`

#### ./src/lib

- contains the shared logic for the application
- this is where you would put utility functions, API calls, and other shared code
- these files are not served to the client
- these files are not imported directly into the application

#### ./src/components

- contains the shared components for the application
- these are the components that are used across multiple routes

#### ./src/routes

- contains the routes for the application
- each route is a Svelte component
- the file name is the route name
- the entry point for the application is `./src/routes/+page.svelte`

#### ./src/routes/+layout.svelte

- the layout component for the application
- wraps the content of each route
- contains the global styles and scripts

#### ./src/app.html

- the main HTML file for the application
- this is where all the content is rendered

#### ./static

- contains the static assets for the application
- this is where you would put images, fonts, and other files
- these files are served as-is
