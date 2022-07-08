<template src="./template.html">

</template>

<script>
export default {
  name: "SwitchableArea-Tab",
  props: ['currentTab'],
  methods: {
    clickTab(key) {
      if (key !== this.currentTab) {
        this.$emit('changeTab', key);
      }
    }
  }
}
</script>

<style scoped lang="scss" src="./style.scss">

</style>