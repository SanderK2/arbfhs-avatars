<template>
  <AvatarProfile :profileObject="profile"/>
  <div class="otherProfiles">
        <div :class="activeProfile == '0' ? 'currentProfile':''" @click="changeProfile('0')">
            <img :src="profileObject['0'].profileImg" alt="">
        </div>
        <div :class="activeProfile == '1' ? 'currentProfile':''" @click="changeProfile('1')">
            <img :src="profileObject['1'].profileImg" alt="">
        </div>
        <div :class="activeProfile == '2' ? 'currentProfile':''" @click="changeProfile('2')">
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
            "https://media.discordapp.net/attachments/1013411019177078815/1051093912405688371/16706706950333662434586405298905.gif",
            "https://i.kym-cdn.com/entries/icons/original/000/038/423/Spamton_screenshot_shop.png",
            "https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/f055370b-a48d-4c77-a02e-b415a802b6d3/derudet-b9b346f7-53a6-4a73-9711-dfdddfc53b90.png/v1/fill/w_1280,h_1033,q_80,strp/don_t_you_want_to_be_a__big_shot___by_cyber_walker_derudet-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTAzMyIsInBhdGgiOiJcL2ZcL2YwNTUzNzBiLWE0OGQtNGM3Ny1hMDJlLWI0MTVhODAyYjZkM1wvZGVydWRldC1iOWIzNDZmNy01M2E2LTRhNzMtOTcxMS1kZmRkZGZjNTNiOTAucG5nIiwid2lkdGgiOiI8PTEyODAifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uub3BlcmF0aW9ucyJdfQ.RmHknLFo66MYaNHfVvo1j9hX47MCttAg2ulOY-1YYic"
          ]
        },
        "1": {
          name: "Dr. Ivo Robotnik",
          ingress: "Dominance, destruction, and complete rule of mobius",
          aboutMe: "I am in like of fried boiled and stoned eggs, i like my eggs on toast and my eggs on pancakes",
          profileImg: "https://i.ytimg.com/vi/tgaUDK3cMq4/hqdefault.jpg",
          backgroundImg: "https://static.tvtropes.org/pmwiki/pub/images/nincombots.jpg",
          text: "WHY is my precious rocketship drifting up into deep space? WHY am i reaching you at the coordinates of the abandoned space station WHY WHY WHY!!!!!",
          imageReel: [
            "https://i.ytimg.com/vi/km6Br9suQ9U/maxresdefault.jpg",
            "https://i1.sndcdn.com/artworks-000119365747-ezy3yn-t500x500.jpg",
            "https://media.tenor.com/a8FAWwmWRisAAAAC/robotnik-aosth.gif",
            "https://64.media.tumblr.com/c16f7330fc246c4ad088fe4ebeba6681/tumblr_pow84hdJjE1sxudx7o1_1280.jpg",
            "https://pbs.twimg.com/media/D9vBcj9UYAAebit.jpg",
            "https://64.media.tumblr.com/3d79d6540275a7eff78cd5461ba88e27/tumblr_ndccstB2UI1sxudx7o1_1280.png"
          ]
        },
        "2": {
          name: "Amogus B. Sussy",
          ingress: "I am sussy. Amogus sussy baka",
          aboutMe: "Amogus. Red sus. Among us. Emergency meeting!!!",
          profileImg: "https://i1.sndcdn.com/artworks-TOJJyHynzM0iRSuW-9URBDA-t500x500.jpg",
          backgroundImg: "https://acf.geeknetic.es/imgri/imagenes/auto/22/04/14/8ys-r6m-among-us-todo-lo-que-necesitas-saber.jpg?f=webp",
          text: "Sussy baka sussy sussy sussy baka sussy baka sussy sussy sussy baka you are being a sussy baka sussy baka sussy sussy sussy baka sussy baka among us bro man you are looking like imposter man you are looking sus bro",
          imageReel: [
            "https://pbs.twimg.com/profile_images/1572281888127193097/y0cpTlQO_400x400.jpg",
            "https://i.kym-cdn.com/photos/images/newsfeed/002/182/169/c10.jpg",
            "https://m.media-amazon.com/images/M/MV5BODEyMmNjNWItMmY1OS00YzQ2LTljODQtNTNkMjU1NTAyZThkXkEyXkFqcGdeQXVyMTQyMjc5NTE3._V1_FMjpg_UX1000_.jpg",
            "https://i.kym-cdn.com/photos/images/newsfeed/002/015/307/543.jpg",
            "https://i.ytimg.com/vi/LZCUgsNrDOQ/maxresdefault.jpg",
            "https://www.mypokecard.com/en/Gallery/my/galery/BoQyE96QLdc3.jpg"
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
