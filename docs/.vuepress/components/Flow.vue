<template>
  <div>
  </div>
</template>

<script>
import { convertCodeToSvg } from 'js2flowchart';
export default {
  name: 'Flow',
  props: {
    code: { type: String, default: '' }
  },
  mounted() {
    const svg = convertCodeToSvg(this.code);
    this.$el.innerHTML = svg;
    console.log(svg);
  }
};
</script>

<style scoped>

</style>