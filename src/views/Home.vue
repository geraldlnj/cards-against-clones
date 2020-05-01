<template>
  <v-content>
    <v-flex d-flex>
      <v-layout wrap>
          <v-flex md4 v-for="card in cards" :key="card.text" class='pa-2 ma-2'>
              <card
                :type="card.type"
                :text="card.text"
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
      },
      {
        type: 'answer',
        text: 'Answer 1',
      },
      {
        type: 'answer',
        text: 'Answer 2',
      },
      {
        type: 'answer',
        text: 'Answer 3',
      },
      {
        type: 'answer',
        text: 'Answer 4',
      },
      {
        type: 'answer',
        text: 'Answer 5',
      },
    ],
  }),
};
</script>
