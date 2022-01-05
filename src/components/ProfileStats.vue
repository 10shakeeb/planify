<template>
  <v-sparkline
    :value="values"
    :color="color"
    smooth="10"
    :fill="false"
    auto-draw
  ></v-sparkline>
</template>

<script>
    export default {
        data() {
            return {
                
            }
        },
        props:{

          color:{
            type:String
            },
            values:{
                type:Array
            }
            }

    }
</script>

<style scoped>

</style>