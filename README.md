# Intro-to-Nuxt-

Nuxt.js is not a server side framework. It runs on the servers. It renders the first page and after the first page is renderd, the Vue.js app takes over.

# Why Nuxt

1)  Server-Side Rendering
2)  Single Page Application (page is loaded only once, components are changing)
4)  Middleware to project authenticated contents 

Difference from other frameworks

1) SEO friendly (power to edit metadata)
2)   Routing is done automatically. 
3)   Hot reloading

Notes
1) Dynamic routes can be added using _name tag.
2)  Directories:- The **pages** directory contains your application's views and routes. The **components** directory is where you put all your Vue.js components which are then imported into your pages. The **assets** directory contains your styles, images, or fonts. The **package**.json file contains all the dependencies and scripts.
3)  Default Layout is applied to every view
4)  The <Nuxt/> component must be added when creating a layout to actually include the page component.


# Pages template
```
<template>
  <h1 class="red">Hello World</h1>
</template>

<script>
  export default {
    head() {
      // Set Meta Tags for this Page
    }
    // ...
  }
</script>

<style>
  .red {
    color: red;
  }
</style>
```
# Default Layout

Adding a default.vue file to the layouts directory will make a default view. The only thing you need to include in the layout is the <Nuxt /> component which renders the page component.

```
<template>
  <Nuxt />
</template>
```
A blog file to be used as a custom layout
```
<script>
  export default {
    layout: 'blog'
    // page component definitions
  }
</script>
```

# Server Vs Browser
Because you are in a Node.js environment you have access to Node.js objects such as **req** and **res**. You can use **window or document** by using the beforeMount or mounted hooks.

```
beforeMount () {
  window.alert('hello');
}
mounted () {
  window.alert('hello');
}
```








