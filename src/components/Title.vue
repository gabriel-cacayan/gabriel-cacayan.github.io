<template>
  <h1
    v-if="type === 'start'"
    class="text-primary text-4xl lg:text-7xl font-bold"
    :class="class"
  >
    &#10094; <slot></slot> &#10095;
  </h1>

  <h1
    v-if="type === 'end'"
    class="text-primary text-4xl lg:text-7xl font-bold text-end"
    :class="class"
  >
    &#10094;&#47; <slot></slot> &#10095;
  </h1>
</template>
<script>
export default {
  props: ["type", "class"],
};
</script>
