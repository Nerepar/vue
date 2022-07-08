<template src="./template.html"/>

<script>
import Area from "@/components/slider/Area/Area";
export default {
  name: "Slider-Controller",
  components: {
    Area
  },
  beforeMount() {
    this.timer = setInterval(this.changeSlide.bind(this), this.delay);
  },
  data() {
    return {
      currentSlide: 'slide-1',
      prefixSlide: 'slide-',
      maxCountSlider: 3,
      timer: null,
      delay: 2500
    }
  },
  methods: {
    changeSlide(isNext = null) {
      if (isNext === null) {
        isNext = true;
        } else {
        if (this.timer) {
          clearInterval(this.timer);
        }
      }
        let slideNumber = Number(this.currentSlide.replace(this.prefixSlide, ''))
        slideNumber += isNext ? 1 : -1;
        if (slideNumber > this.maxCountSlider) {
          slideNumber = 1;
        } else if (slideNumber <1) {
          slideNumber = this.maxCountSlider;
        }

        this.currentSlide = this.prefixSlide + slideNumber;
    }
  }
}
</script>

<style scoped src="./style.scss" lang="scss"></style>