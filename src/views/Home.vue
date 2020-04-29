<template>
  <v-content>
    <Card type="answer"/>
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
};
</script>
