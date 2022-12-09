<template>
  <AvatarProfile :profileObject="profile"/>
  <div class="otherProfiles">
        <div class="profileCircle currentProfile" @click="changeProfile('0')">
            <img :src="profileObject['0'].profileImg" alt="">
        </div>
        <div class="profileCircle" @click="changeProfile('1')">
            <img :src="profileObject['1'].profileImg" alt="">
        </div>
        <div class="profileCircle" @click="changeProfile('2')">
            <img :src="profileObject['2'].profileImg" alt="">
        </div>
    </div>
</template>

<script>
import AvatarProfile from './pages/AvatarProfile.vue'

export default {
  name: 'App',
  components: {
    AvatarProfile
  },
  computed: {
    profile(){
      return this.profileObject[this.activeProfile]
    },
  },
  methods: {
    changeProfile(id){
      this.activeProfile = id;
    }
  },
  data() {
    return {
      activeProfile: "0",
      profileObject:  {
        "0": {
          name: "Brødskive",
          ingress: "Drag, sminke, non-binary rage.",
          aboutMe: "Jeg liker å danse og sånn da. Fester er kult også.",
          profileImg: "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
          imageReel: [
            "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
            "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
            "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ"
          ]
        },
        "1": {
          name: "Smurt skive",
          ingress: "Drag, sminke, non-binary rage.",
          aboutMe: "Jeg liker å danse og sånn da. Fester er kult også.",
          profileImg: "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
          imageReel: [
            "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
            "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
            "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ"
          ]
        },
        "2": {
          name: "Sandwhich",
          ingress: "Drag, sminke, non-binary rage.",
          aboutMe: "Jeg liker å danse og sånn da. Fester er kult også.",
          profileImg: "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
          imageReel: [
            "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
            "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
            "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ"
          ]
        }
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
  display: flex;
}

body {
  margin: 0;
}
</style>
