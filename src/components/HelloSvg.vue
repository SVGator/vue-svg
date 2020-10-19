<template>
  <div>
    <img
      src="https://cdn.svgator.com/assets/logo.png"
      alt="SVGator"
      height="30px"
    />
    <FerrisWheel />
  </div>
</template>

<script>
import FerrisWheel from "./SvgComponents/FerrisWheel";

export default {
  name: "HelloSvg",
  components: {
    FerrisWheel,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img {
  position: absolute;
  top: 20px;
  left: 30px;
}
svg {
  width: 100vw;
  height: 100vh;
}
</style>
