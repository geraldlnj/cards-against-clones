<template>
  <v-content>
    <v-flex d-flex>
      <v-layout wrap>
          <v-flex md4 v-for="card in cards" :key="card.text" class='pa-2 ma-2'>
              <card
                :id="card.text"
                :type="card.type"
                :text="card.text"
                :flipped="card.flipped"
              />
          </v-flex>
      </v-layout>
    </v-flex>
  </v-content>
</template>

<script>
// @ is an alias to /src
import Card from '@/components/Card.vue';

export default {
  name: 'Home',
  components: {
    Card,
  },
  data: () => ({
    cards: [
      {
        type: 'question',
        text: 'Question 1',
        flipped: false,
      },
      {
        type: 'answer',
        text: 'Answer 1',
        flipped: false,
      },
      {
        type: 'answer',
        text: 'Answer 2',
        flipped: false,
      },
      {
        type: 'answer',
        text: 'Answer 3',
        flipped: false,
      },
      {
        type: 'answer',
        text: 'Answer 4',
        flipped: false,
      },
      {
        type: 'answer',
        text: 'Answer 5',
        flipped: false,
      },
    ],
  }),
};
</script>
