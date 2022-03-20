<template>
  <div>
    <slot name="default"></slot>

    <h2 :style="{ color: '#' + cor, fontSize: valor + 'px' }">
      <slot name="text"></slot>
    </h2>
  </div>
</template>

<script>
export default {
  name: "Main",
  props: {
    cor: String,
    valor: Number,
  },
};
</script>

<style >
</style>
