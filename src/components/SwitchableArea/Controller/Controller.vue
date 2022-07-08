<template src="./template.html">

</template>

<script>
import Area from "@/components/SwitchableArea/Area/Area";
import Tab from "@/components/SwitchableArea/Tab/Tab";

export default {
  name: "SwitchableArea-Controller",
  components: {
    Area, Tab
  },
  data() {
    return {
      currentTab: "tab-1"
    }
  },
  methods: {
    changeTab(key) {
      this.currentTab = key;
    }
  }
}
</script>

<style scoped lang="scss" src="./style.scss">

</style>