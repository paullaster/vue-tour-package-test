<template>
  <div id="app">
    <h1>Testing vue tour package for vue v2</h1>
    <div id="id1"> This is the first place</div>
    <div id="id2"> This is the second place</div>
    <div id="id3"> This is the third place</div>
    <div id="id4"> This is the fourth place</div>
    <div id="id5"> this is the last place</div>

    <v-tour name="myTour" :steps="steps"></v-tour>
  </div>
</template>

<script>
  export default {
    name: "App",
    data(){
      return{
        steps: [
          {
            target: '#v-step-0',  // We're using document.querySelector() under the hood
            content: `Discover <strong>Vue Tour</strong>!`
          },
          {
            target: '.v-step-1',
            content: 'An awesome plugin made with Vue.js!'
          },
          {
            target: '[data-v-step="2"]',
            content: 'Try it, you\'ll love it!<br>You can put HTML in the steps and completely customize the DOM to suit your needs.',
            params: {
              placement: 'top'
            }
          }
        ]
      }
    }
  }
</script>
