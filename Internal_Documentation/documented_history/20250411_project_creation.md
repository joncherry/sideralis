- installed node v23.11.0 and npm 10.9.2 using https://nodejs.org/en/about/previous-releases with the node-v23.11.0-linux-x64.tar.gz file extracted to my home directory and then adding the bin folder to my PATH var in `~/.zshrc`.
- created the initial scaffolding with https://www.electronforge.io/guides/framework-integration/vue-3
    - `npx create-electron-app@latest my-vue-app --template=vite`
    ```bash
    npm install vue
    npm install --save-dev @vitejs/plugin-vue
    ```
    - and used these files:
    
    ```hmtl
    <!-- ./index.html -->
    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="UTF-8" />
        <title>Hello World!</title>
    </head>
    <body>
        <div id="app"></div>
        <script type="module" src="/src/renderer.js"></script>
    </body>
    </html>
    ```

    ```html
    <!-- ./src/App.vue -->
    <template>
        <h1>Goodbye Cruel World!</h1>
        <p>Welcome to your Electron application.</p>
    </template>

    <script setup>
    console.log('👋 This message is being logged by "App.vue", included via Vite');
    </script>
    ```

    ```javascript
    // ./src/renderer.js
    import { createApp } from 'vue';
    import App from './App.vue';

    createApp(App).mount('#app');
    ```

    ```javascript
    import { defineConfig } from 'vite';
    import vue from '@vitejs/plugin-vue';

    // https://vitejs.dev/config
    export default defineConfig({
    plugins: [vue()]
    });
    ```
- Then I added vuetify with https://vuetifyjs.com/en/getting-started/installation/#existing-projects
    - `npm i vuetify`
    - and overwrote renderer.js with:
    ```javascript
    import { createApp } from 'vue'

    // Vuetify
    import 'vuetify/styles'
    import { createVuetify } from 'vuetify'
    import * as components from 'vuetify/components'
    import * as directives from 'vuetify/directives'

    // Components
    import App from './App.vue'

    const vuetify = createVuetify({
    components,
    directives,
    })

    createApp(App).use(vuetify).mount('#app')
    ```
- Then I added prettier with `npm install prettier`, then I added the following to the `scripts` section of the `package.json`
```
    "format": "prettier --write src/"
```
