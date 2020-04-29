<template>
  <vue-flip
    :active-click="true"
    height="384px"
    width="240px"
  >
    <template v-slot:front>
      <CardFace v-bind:type="type"/>
    </template>
    <template v-slot:back>
      <CardBack v-bind:type="type"/>
    </template>
  </vue-flip>
</template>

<script lang="ts">
import Vue from 'vue';
// eslint-disable-next-line @typescript-eslint/ban-ts-ignore
// @ts-ignore
import VueFlip from 'vue-flip';
import CardBack from '@/components/CardBack.vue';
import CardFace from '@/components/CardFace.vue';


export default Vue.extend({
  name: 'Card',
  components: {
    VueFlip,
    CardBack,
    CardFace,
  },
  props: {
    type: {
      default: 'question',
      type: String,
      required: true,
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
