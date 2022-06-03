<template>
  <div class="about">
    <h1>This is an about page</h1>
    <component
      :is="selectedComponent"
      title="About title"
      @onStart="onStartGame"
    ></component>
  </div>
</template>
<script>
import StartScreen from "@/components/StartScreen.vue";
import GameScreen from "@/components/GameScreen";
export default {
  data() {
    return {
      selectedComponent: "StartScreen",
    };
  },
  components: {
    StartScreen,
    GameScreen,
  },
  methods: {
    onStartGame() {
      console.log("start game");
      this.selectedComponent = "GameScreen";
    },
  },
};
</script>
