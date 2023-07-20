<template>
  <p>{{ age }}</p>
  <button type="button" @click="changeAge">Update</button>
  <button type="button" @click="changeAgeCB(3)">Update</button>
</template>

<script>
export default {
    name:"User",
    data () {
        
        return {}
    },
    props:{
 
        age:{
            type:Number,
            default:100,
            validator(value){
            return value>2
        }
        
        },
        changeAgeCB:{
            type:Function
        }
    },
    methods:{
        changeAge(){
            this.$emit("change-age")
        }
    }
}
</script>

<style >

</style>