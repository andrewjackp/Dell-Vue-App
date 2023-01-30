<template>
  <BackgroundVidVue />
  <NicolePortal1
    v-for="post in posts"
    :key="post.id"
    :paragraph="post.paragraph"
  />
  <RightSidePopUps />
</template>
<script>
import HelloWorld from "./components/HelloWorld.vue";
import BackgroundVidVue from "./components/BackgroundVid.vue";
import NicolePortal1 from "./components/NicolePortal1.vue";
import RightSidePopUps from "./components/RightSidePopUps.vue";

export default {
  name: "App",
  components: {
    BackgroundVidVue,
    // HelloWorld,
    NicolePortal1,
    RightSidePopUps,
  },
  data() {
    return {
      posts: [
        {
          id: 1,
          paragraph:
            "Back in January, Nicole attended CES, where she was able to explore the Dell booth.",
        },
        {
          id: 2,
          paragraph:
            "Dell hosted an interactive experience that showed how integrated hardware management and machine learning can help healthcare professionals track and measure treatment efficacy across hospital systems.",
        },
        {
          id: 3,
          paragraph:
            "Months later, when Nicole is tasked with a technology transition at her hospital, she remembers the impressive Dell experience at CES.",
        },
        {
          id: 4,
          paragraph:
            "After Nicole talks with a Dell representative about her goals, concerns and needs, the representative suggests Dell&apos; white-glove service. ",
        },
      ],
    };
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
