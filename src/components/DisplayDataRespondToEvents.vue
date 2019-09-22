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
            <input type="text" style="margin-right: 20px;" placeholder="ONE WAY BINDED"/>
            <label>{{message}}</label>
        </div>
        <br/>
        <div id="inputBoxDiv">
            <button style="margin-right: 20px;" @click="addNumber">Add Number:</button>
            <label>{{counter}}</label>
        </div>
        <br/>
        <div id="inputBoxDiv">
            <input type="text" v-model="twoWayBindedMessage " style="margin-right: 20px;" placeholder="TWO WAY BINDED"/>
            <label>{{twoWayBindedMessage}}</label>
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
          twoWayBindedMessage: '', 
          counter: 0,
          google: "https://google.com",
          facebook: "https://facebook.com"
      }
  },

  methods: {
      addNumber() {
          this.counter++;
      }
  }
}
</script>

<style scoped>
</style>
