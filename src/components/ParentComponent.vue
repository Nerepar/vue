<template>
  <ChildComponent @msgTextChange="_msgTextChange" :textMsg="textMsg"/>
</template>

<script>
import ChildComponent from "@/components/ChildComponent";
export default {
  name: "ParentComponent",
  components: {
    ChildComponent,
  },
  data () {
    return {
      textMsg: 'Сообщение родителя'
    }
  },
  methods: {
    _msgTextChange(text) {
      this.textMsg = text;
    }
  }
}
</script>

<style scoped>

</style>