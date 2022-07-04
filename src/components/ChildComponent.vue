<template>
  <div class="ChildComponentWrapper">
    <span>{{ textMsg }} </span>
    <button @click="_changeText">Change</button>
  </div>
</template>

<script>
export default {
  name: "ChildComponent",
  props: ['textMsg'],
  methods: {
    _changeText() {
      this.$emit('msgTextChange', 'Дочернее сообщение');
    }
  }
}
</script>

<style scoped>

</style>