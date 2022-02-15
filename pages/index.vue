<template>
   <div class="homePage">
      <Quote :data="quote.data[0]" info/>
   </div>
</template>

<style lang="scss">
@import "~/assets/scss/pages/home";
</style>

<script>
import Quote from "../components/quote"
import { randomQuote } from "quotegarden"

export default {
   components: { Quote },
   async asyncData() {
      const quote = await randomQuote()
      return {quote}
   },
   data() {
      return {
         quote: null
      }
   },
   mounted() {
      this.$nuxt.$on("random", async () => this.quote = await randomQuote())
   },
}
</script>
