<script>

import Greeting from './components/Greeting.vue';
import User from './components/User.vue';
export default {
  name: "App",
  data(){
    return{
      age:20
    }
  },
  methods:{
    changeAgeEmit(){
      this.age=this.age*3

    },
    changeAgeCB(num){
      this.age+=num
    }
  },
  components: {
    Greeting,User
  },

};
</script>

<template>
  <Greeting :age="age"></Greeting>
  <User :age="age" @change-age="changeAgeEmit" :changeAgeCB="changeAgeCB"></User>
</template>

<style scoped></style>
