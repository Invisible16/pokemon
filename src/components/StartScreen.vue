<template>
  <div class="start-screen">
    start {{ title }}
    <button @click="$emit('onStart')">Start game</button>
  </div>
</template>

<script>
export default {
  name: "StartScreen",
  props: ["title", "onStart"],
};
</script>

<style></style>
