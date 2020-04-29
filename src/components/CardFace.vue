<template>
  <v-container class='pa-0'>
    <div class='cardContainer'>
      <div v-bind:class="classObject">
        <p class='text'>Cards Against Clones</p>
      </div>
    </div>
  </v-container>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'CardFace',
  props: {
    type: {
      default: 'question',
      type: String,
    },
    text: String,
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
    font-size: 32px;
    padding-top: 7%;
    padding-left:7%;
    padding-right:7%;
    word-wrap: break-word;
  }
  .rounded-card{
    border-radius:50px;
  }

</style>
