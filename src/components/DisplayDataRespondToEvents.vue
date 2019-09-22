<template>
    <div id="MainDiv">
        <div id="TitleDiv">
            <h1>{{staticPageTexts.title}}</h1>
        </div>
        <div id="simpleLinkDiv">
            <a :href="google" target="_blank">Take me to google</a>
            <br/>
            <a v-bind:href="facebook" target="_blank">Take me to facebook</a>
        </div>
        <br/>
        <div id="inputBoxDiv">
            <input type="text" style="margin-right: 20px;" placeholder="Insert Msg"/>
            <label>{{message}}</label>
        </div>
    </div>
</template>

<script>
export default {
  name: 'DisplayDataRespondToEvents',
   
  data() {
      return {
          staticPageTexts: {
              title: "COOL TITLE !!"
          },
          message: '',
          google: "https://google.com",
          facebook: "https://facebook.com"
      }
  }
}
</script>

<style scoped>
</style>
