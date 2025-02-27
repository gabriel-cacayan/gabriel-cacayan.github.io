<template>
  <h1 class="text-primary text-4xl lg:text-7xl font-bold" :class="class">
    <slot></slot>
  </h1>
</template>
<script>
export default {
  props: ["class"],
};
</script>
