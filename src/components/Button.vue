<template>
  <button class="btn" :class="'bg-red-400 font-bold text-3xl'">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: String,
    color: String
  }
};
</script>
