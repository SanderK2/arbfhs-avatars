<template>
  <AvatarProfile :profileObject="profileObject"/>
</template>

<script>
import AvatarProfile from './pages/AvatarProfile.vue'

export default {
  name: 'App',
  components: {
    AvatarProfile
  },
  data() {
    return {
        profileObject: {
          name: "Brødskive",
          ingress: "Drag, sminke, non-binary rage.",
          aboutMe: "Jeg liker å danse og sånn da. Fester er kult også.",
          profileImg: "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
        }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

body {
  margin: 0;
}
</style>
