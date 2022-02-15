<template>
   <div class="quote">
      <div class="content">
         “{{ data.quoteText }}”
      </div>
      <div class="infos" v-if="info">
         <div class="left">
            <div class="author">{{ data.quoteAuthor }}</div>
            <div class="genre">{{ data.quoteGenre }}</div>
         </div>
         <span class="material-icons-round">arrow_forward</span>
      </div>
   </div>
</template>

<style lang="scss">
@import "style";
</style>

<script>
import Vue from "vue"

export default Vue.extend({
   name: "Quote",
   props: {
      data: Object,
      info: Boolean
   }
})
</script>
