<template>
  <div>
    <SideBar/>
    <ListCharactersComponent/>
  </div>
</template>

<script>
import SideBar from './components/SideBar.vue';
import ListCharactersComponent from './components/ListCharactersComponent.vue';

import axios from "axios";
 
export default {
  name: 'App',
  components: {
    SideBar,
    ListCharactersComponent,
  },
  created() {
    axios
        .get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((res) => {
          console.log(res);
        });
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
