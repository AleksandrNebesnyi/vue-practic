<template>
  <Title></Title>
  <Button v-on:click="increment" type="button" outlined>Clikk</Button>
  <h1>{{ title }}</h1>
  <DirectiveTest />
</template>

<script>
import Title from './components/Title.vue';
import Button from './components/Button.vue';
import DirectiveTest from './components/DirectiveTest.vue';

export default {
  name: 'App',
  components: {
    Title,
    Button,
    DirectiveTest,
  },
  data() {
    return {
      amountOfClicks: 1,
    };
  },
  computed: {
    title() {
      return `Amount click ${this.amountOfClicks}`;
    },
  },
  methods: {
    increment() {
      this.amountOfClicks += 1;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
