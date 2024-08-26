<template>
<div>
            <h2 id=title class="text-center border mb-5" style="font-size:40px">{{title}}</h2>
            <v-carousel cycle  :show-arrows="false" width="100%"  height="300" hide-delimiters interval=2000 >
              <v-carousel-item class="mt-5 " v-for=" skill in skills" :key="skill">
                <v-img :src="skill"></v-img>
              </v-carousel-item>
            </v-carousel>
        
        
     
</div>
</template>

<script>
export default {
data:()=>({}),
    props:["skills","title"]
}
</script>

<style scoped>
#title:hover{
background-color: lightgreen;
}
</style>