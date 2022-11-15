<template>
  <div id="app">
    <button @click="load">load</button>
    <LoadingPage class="loading" v-if="!isLoaded"/>
    <MenuBar />
    <router-view/>
  </div>
</template>

<script>
import LoadingPage from '@/components/LoadingPage'
import MenuBar from '@/components/MenuBar'

export default {
  name: 'App',
  data() {
    return {
      isLoaded: false
    }
  },
  components: {
    LoadingPage,
    MenuBar,
  },
  methods: {
    load() {
      this.isLoaded = !this.isLoaded
    }
  },
}
</script>

<style>
body {
  background-color: gray;

}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* display: grid; */
  /* grid-template-areas: ""; */
  position: relative;
}

.loading {
  width: 300px;
  position: absolute;
  top: 500px;
  left: 1200px;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
