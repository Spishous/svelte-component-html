# svelte-component-html
create a reusable component js with svelte

# Step
Setup svelte project with svelte:
```
npm create vite
```
set this code in vite.config.js:

```
import { defineConfig } from 'vite'
import { svelte } from '@sveltejs/vite-plugin-svelte'
import { resolve } from "path"

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [svelte()],
  build: {
    rollupOptions: {
      output: {
        format: "iife",
        dir: resolve(__dirname, "./dist"),
        entryFileNames: "main.js",
      },
    },
  },
})
```

Change the html ID target:
```
  target: document.getElementById('my_component'),
```

Build project with:
```
npm run build
```

# Finaly

You got a main.js file who you should add to you next website html
