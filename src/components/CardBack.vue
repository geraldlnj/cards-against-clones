<template>
  <v-container class='pa-0'>
    <div class='cardContainer'>
      <div :class="classObject">
        <p class='text'>{{text}}</p>
      </div>
    </div>
  </v-container>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'CardBack',
  props: {
    type: {
      default: 'question',
      type: String,
      required: true,
    },
    text: {
      default: 'Placeholder Question',
      type: String,
      required: true,
    },
  },

  data: () => ({
  }),
  computed: {
    classObject() {
      return {
        card: true,
        question: this.type === 'question',
      };
    },
  },
  methods: {
  },
});
</script>

<style scoped>
  .card{
  /* Card Sizing */
  width: 2.5in;
  height: 4in;
  border-radius: .25in;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);

  /* Display Properties */
  float: left;
  /* margin: 10px; */
  }

  .question{
    border: 3px solid black;
    color: white;
    background: black;
  }
  .text{
    /*font information*/
    font-family: Helvetica,sans-serif;
    font-weight: bolder;
    font-size: 26px;
    padding-top: 7%;
    padding-left:7%;
    padding-right:7%;
    word-wrap: break-word;

    /* unhighlightable text */
    -webkit-touch-callout: none; /* iOS Safari */
    -webkit-user-select: none; /* Safari */
    -khtml-user-select: none; /* Konqueror HTML */
    -moz-user-select: none; /* Old versions of Firefox */
    -ms-user-select: none; /* Internet Explorer/Edge */
    user-select: none; /* Non-prefixed version, currently supported by Chrome, Opera and Firefox */
  }
  .rounded-card{
    border-radius:50px;
  }

</style>
