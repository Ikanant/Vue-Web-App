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
        <br/>
        <div id="radioButtonDiv">
            <label>Pick bar color:</label>
            <label for="color-r">
                <input type="radio" id="color-red" value="red" v-model="barColor"/>R
            </label>
            <label for="color-b">
                <input type="radio" id="color-blue" value="blue" v-model="barColor"/>B
            </label>
            <label for="color-g">
                <input type="radio" id="color-green" value="green" v-model="barColor"/>G
            </label>
            <br/>
            <div id="colorBar" class="barColor" v-bind:style="{'background-color': barColor}"></div>
        </div>
        <br/>
        <div id="radioButtonDiv">
            <label>Pick another color:</label>
            <select v-model="secondBarColor" v-on:keyup.esc="clearSelect">
                <option value="red">red</option>
                <option value="blue">blue</option>
                <option value="green">green</option>
            </select>
            <br/>
            <label>Bar will be red if nothing selected: {{secondBarColor}}</label>
            <div id="secondColorBar" v-bind:class="{ invalid : secondBarColor=='' }" class="barColor"></div>
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
          barColor: 'red',
          secondBarColor: '',
          google: "https://google.com",
          facebook: "https://facebook.com"
      }
  },

  methods: {
      addNumber() {
          this.counter++;
      },
      clearSelect() {
          this.secondBarColor = '';
      }
  }
}
</script>

<style scoped>
    .barColor {
        height: 10px;
        width: 100px;
        margin-left: 50%;
    }
    .invalid {
        background-color: blueviolet
    }
</style>
