<template>
  <CreditCard
    v-for="card in cards"
    v-bind:key="card.id"
    v-bind:name="card.name"
    v-bind:slug="card.slug"
    v-bind:img="card.image"
    v-bind:brand="card.brand"
    v-bind:category="card.category"
    v-bind:limit="card.limit"
    v-bind:fee="card.fee"
  ></CreditCard>
</template>

<script>
import CreditCard from './CreditCard.vue'

export default {
  name: 'List',
  components: {
    CreditCard
  },
  props: {
    cards: {
      type: Array,
      required: true,
      default: () => [],
    },
  }
}
</script>
