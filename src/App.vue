<template>
  <div id="app">
    <h1 :style="titleStyle">Пример приложения с использованием Vuex</h1>
    <p>Счетчик: {{ $store.state.count }}</p>
    <button @click="increment" :style="buttonStyle">Увеличить</button>
    <button @click="decrement" :style="buttonStyle">Уменьшить</button>
    <button @click="reset" :style="resetButtonStyle">Сбросить</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      buttonStyle: {
        backgroundColor: '#4CAF50',
        color: 'white',
        padding: '10px 20px',
        border: 'none',
        borderRadius: '5px',
        cursor: 'pointer',
        marginRight: '10px'
      },
      titleStyle: {
        color: '#009688',
      },
      resetButtonStyle: {
        backgroundColor: '#f44336',
        color: 'white',
        padding: '10px 20px',
        border: 'none',
        borderRadius: '5px',
        cursor: 'pointer',
      }
    };
  },
  methods: {
    increment() {
      this.$store.commit('increment');
    },
    decrement() {
      this.$store.commit('decrement');
    },
    reset() {
      this.$store.commit('reset');
    }
  },
};
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  text-align: center;
}
</style>