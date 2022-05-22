<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>

    <!-- 1. -->
    <AppPosts />
    <!-- or -->
    <!-- <app-posts /> -->

    <!-- 2. -->
    <AppPosts2 name='asdasd' :name2='name2'>
        <div>children</div>

        <template #children2>
            <div>children2</div>
        </template>

        <template #children3>
            <div>children3</div>
        </template>
    </AppPosts2>

  
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import AppPosts from './components/AppPosts.vue'
import AppPosts2 from './components/AppPosts2.vue'

export default {
    name: 'App',

    components: {
      HelloWorld,
      AppPosts,
      AppPosts2,
    },

    props: {
    
    },

    data() {
        return {
            name2: 'asd2asd2',
        }
    },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
