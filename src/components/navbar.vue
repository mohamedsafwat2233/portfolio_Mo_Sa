<template>
  <v-app-bar app color="black" flat class="px-12">
  <v-btn >
    <v-icon color="green" size=50> fas fa-code</v-icon>
  </v-btn>
    <h1 class="my-4 mb-0">portfolio</h1>
  <v-spacer></v-spacer>
      <v-btn text @click="scroll('home')" >Home</v-btn>
      <v-btn text @click="scroll('skills')"  >Skills</v-btn>
      <v-btn text @click="scroll('about')"  >About</v-btn>
      <!-- <v-btn text @click="scroll('portfolio')"  >Portfolio</v-btn>
      <v-btn text @click="scroll('services')" > projects</v-btn>
      <v-btn text @click="scroll('contact')"  > Contact</v-btn> -->
  </v-app-bar>
</template>

<script>

export default {
methods:{
   scroll(refNmae) {
    let element=document.getElementById(refNmae);
    element.scrollIntoView({behavior:"smooth"})
  }
}
}
</script>

<style >

</style>