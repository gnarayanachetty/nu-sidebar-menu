<template>
  <div>
    <h2>Installation</h2>
    <p>Use npm to install plugin</p>
    <prism-code lang="bash">
      {{ `npm i nu-menu --save` }}
    </prism-code>
    <p>Import the plugin globally</p>
    <prism-code lang="js">
      {{
        `import { createApp } from 'vue'
import App from './App.vue'
import NuMenu from 'nu-menu'
import 'nu-menu/dist/nu-menu.css'

const app = createApp(App)
app.use(NuMenu)
app.mount("#app")`
      }}
    </prism-code>
    <p>Or import the component locally.</p>
    <prism-code lang="js">
      {{
        `import { SidebarMenu } from 'nu-menu'
import 'nu-menu/dist/nu-menu.css'
export default {
  components: {
    SidebarMenu
  }
}`
      }}
    </prism-code>
  </div>
</template>
