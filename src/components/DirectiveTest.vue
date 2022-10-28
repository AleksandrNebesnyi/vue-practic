<template>
  <div v-if="isVisible">
    <h1 v-show="false">Derectives</h1>
    <ul>
      <template v-for="fruit in fruits">
        <li v-if="fruit === 'banana'" :key="fruit">{{ fruit }}</li>
      </template>
    </ul>

    <ul>
      <li v-for="(car, key) in cars" :key="car.color">{{ key }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'directiveTest',
  data() {
    return {
      isVisible: true,
      fruits: ['kiwi', 'banana', 'apple'],
      cars: {
        audi: {
          color: 'red',
        },
        bmw: {
          color: 'black',
        },
      },
    };
  },
};
</script>

<style lang="scss" scoped></style>
