<template>
  <div class="Examlpe__wrapper">
    {{ text }}
    <button @click="_changeText"> Нажми меня </button>
  </div>
</template>

<script>
export default {
  name: 'ExampleMy',
  beforeMount() {
    console.log('beforeMount');
  },
  beforeUpdate() {
    console.log('beforeUpdate');
  },
  beforeUnmount () {
    console.log('beforeUnmount');
  },

  data () {
    return {
      text: 'Привет'
    }
  },

  methods: {
    _changeText() {
      this.text = 'Пока!';
    }
  }
}
</script>

<style lang="scss" scoped>

</style>