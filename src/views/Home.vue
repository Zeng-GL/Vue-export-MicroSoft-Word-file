<template>
  <div class="home">
    <wordexport />
  </div>
</template>

<script>
// @ is an alias to /src
import wordexport from "../components/wordexport.vue"

export default {
  name: 'Home',
  components: {
    wordexport
  }
}
</script>
