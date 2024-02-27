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

5. Open your browser and navigate to `localhost:5000`

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
