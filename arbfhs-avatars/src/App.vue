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
          name: "Spamton G Spamton",
          ingress: "SALESMAN 1992",
          aboutMe: "I'M A [BIGSHOT] YOU KNOW, A GREAT SALESMAN, I GOT [DEALS]",
          profileImg: "https://static1.cbrimages.com/wordpress/wp-content/uploads/2022/09/deltarune-spamton-painting.jpg",
          backgroundImg: "https://i.kym-cdn.com/entries/icons/original/000/038/423/Spamton_screenshot_shop.png",
          text: "ARE YOU A [LITTLE SPONGE]. ARE YOU LOOKING FOR A GREAT [DEALS]. THEN I GOT FOR YOU [HYPERLINK BLOCKED]. INTRODUCING SPAMTON G SPAMTON'S WONDERFUL EXTRAORDINARY [SATURDAY NIGHTS] [[DEALS]]",
          imageReel: [
            "https://carboncostume.com/wordpress/wp-content/uploads/2022/08/spamton-g-spamton-from-deltarune-2.jpg",
            "https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/a00f3d31-4c4e-4c44-a00b-767b20311274/df9f4ha-dbbb0f35-54d8-4014-aa03-3a3cd7bc697b.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcL2EwMGYzZDMxLTRjNGUtNGM0NC1hMDBiLTc2N2IyMDMxMTI3NFwvZGY5ZjRoYS1kYmJiMGYzNS01NGQ4LTQwMTQtYWEwMy0zYTNjZDdiYzY5N2IucG5nIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.riyw1pE0wmXWYDTbpcpc4uirwIJRSTA6M0dqJqlfC7w",
            "https://deltarune.com/assets/sweepstakes/auction-mona-1.jpg",
            "https://i1.sndcdn.com/artworks-YQUOjcyTCJIDH1UH-Qhk3EA-t500x500.jpg",
            "https://i.kym-cdn.com/entries/icons/original/000/038/423/Spamton_screenshot_shop.png",
            "https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/f055370b-a48d-4c77-a02e-b415a802b6d3/derudet-b9b346f7-53a6-4a73-9711-dfdddfc53b90.png/v1/fill/w_1280,h_1033,q_80,strp/don_t_you_want_to_be_a__big_shot___by_cyber_walker_derudet-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTAzMyIsInBhdGgiOiJcL2ZcL2YwNTUzNzBiLWE0OGQtNGM3Ny1hMDJlLWI0MTVhODAyYjZkM1wvZGVydWRldC1iOWIzNDZmNy01M2E2LTRhNzMtOTcxMS1kZmRkZGZjNTNiOTAucG5nIiwid2lkdGgiOiI8PTEyODAifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uub3BlcmF0aW9ucyJdfQ.RmHknLFo66MYaNHfVvo1j9hX47MCttAg2ulOY-1YYic"
          ]
        },
        "1": {
          name: "Smurt skive",
          ingress: "Drag, sminke, non-binary rage.",
          aboutMe: "Jeg liker å danse og sånn da. Fester er kult også.",
          profileImg: "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
          backgroundImg: "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
          text: "Lorizzle ipsum dolizzle sizzle amizzle, consectetuer adipiscing elit. Nullam sapizzle velit, aliquet volutpizzle, suscipizzle quis, gravida yo, stuff. Pellentesque away check out this. Sed erizzle. Da bomb izzle dolor dapibizzle tempizzle fizzle.",
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
          backgroundImg: "https://gfx.nrk.no/HliIdgQAG0Fs-Pyur2HzUQdvQ_HP06QIPyWNi7h2vOXQ",
          text: "Lorizzle ipsum dolizzle sizzle amizzle, consectetuer adipiscing elit. Nullam sapizzle velit, aliquet volutpizzle, suscipizzle quis, gravida yo, stuff. Pellentesque away check out this. Sed erizzle. Da bomb izzle dolor dapibizzle tempizzle fizzle.",
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
  overflow-x: hidden;
}

body {
  margin: 0;
}
</style>
