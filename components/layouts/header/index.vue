<template>
   <header>
      <div class="randomButton" @click="random">random <span class="material-icons">autorenew</span></div>
   </header>
</template>

<style lang="scss">
header {
   display: flex;
   align-items: center;
   justify-content: flex-end;

   .randomButton {
      display: flex;
      align-items: center;
      gap: 11px;
      padding: 30px 50px;

      cursor: pointer;

      font: {
         weight: 500;
         size: 18px;
      };
   }
}
</style>

<script>
import Vue from "vue"

export default Vue.extend({
   name: "Header",
   methods: {
      random() {
         this.$nuxt.$emit("random")
      }
   }
})
</script>
