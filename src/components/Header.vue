<template>
  <div class="hello">
    <div id="nav">
      <router-link to="/">My Investments</router-link> |
      <router-link to="/about">About</router-link>
      <b-button variant="success" v-b-modal.addPortfolioflag
        >Add portfolio</b-button
      >
      <AddPortfolio />
    </div>
    <router-view />
  </div>
</template>

<script>
import AddPortfolio from "./AddPortfolio.vue";

export default {
  components: { AddPortfolio },
  name: "Header",
  data: function() {
    return {
      addPortfolioflag: false,
    };
  },
  methods: {
    addPortfolio: function() {
      this.addPortfolio = true;
    },
  },
};
</script>


