<template>
    <div id="simpleLinkDiv">
        <a :href="google" target="_blank">Take me to google</a>
        <br/>
        <a :href="facebook" target="_blank">Take me to facebook</a>
    </div>
</template>

<script>
export default {
  name: 'DisplayDataRespondToEvents',
  data() {
      return {
          google: "https://google.com",
          facebook: "https://facebook.com"
      }
  }
}
</script>

<style scoped>
</style>
