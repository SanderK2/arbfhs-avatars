<template>
    <div class="mainProfile">
        <div class="profile">
    <div>
        <div>

        </div>
        <img class="header-image" :src="profileObject.backgroundImg" alt="">
        <div class="blergh">
            <img :src="profileObject.profileImg" alt="" class="profile-pic">
            <div>
                <h1>{{profileObject.name}}</h1>
                
            </div>
        </div>
    </div>
    
    <div class="profileUnder">
        <div class="about">
            <h2>{{profileObject.ingress}}</h2>
            <p>{{profileObject.aboutMe}}</p>
        </div>
        <div class="moreAbout">
            {{ profileObject.text }}
        </div>
    </div>
    <div class="photoSection">
        <h3>BILDEGALLERI</h3>
        <div class="photos">
            <div v-for="(imgg, index) in profileObject.imageReel" :key="index">
                <a :href="imgg" target="_blank"><img :src="imgg" alt=""></a>
            </div>
        </div>
    </div>
    </div>
    
    </div>
    
</template>
<script>

export default {
    name: "AvatarProfile",
    props: {
        profileObject: {
            type: Object,
            required: true
        }
    },
}
</script>

<style>
    .blergh {
        padding-top: 8em;
        height: 15em;
        display: flex;
        align-items: flex-end;
        color: white;
        padding-bottom: 1em;
    }

    .blergh div {
        margin-left: -1.5em;
    }

    h1 {
        margin: 0;
        filter: drop-shadow(4px 4px 10px black);
    }

    h2, p {
        text-align: center;
        margin: 0;
        color: black;
    }

    .header-image {
        position: absolute;
        z-index: -1;
        width: 90vw;
        height: 25em;
        object-fit: cover;
    }
    .profile-pic {
        margin-left: 15px;
        border-radius: 100%;
        width: 15em;
        height: 15em;
        object-fit: cover;
        vertical-align: middle;
        display: block;
        overflow: hidden;
        filter: drop-shadow(4px 4px 10px black);
    }

    .mainProfile {
        display: flex;
    }

    .profile {
        width: 90vw;
    }

    .profileUnder {
        display: flex;
    }

    .otherProfiles {
        width: 10vw;
        padding-top: 10px;
        background-color: #f1faee;
        display: flex;
        flex-direction: column;
    }

    .otherProfiles div {
        border-left: solid 10px #f1faee;
        padding: 3px;
    }

    .otherProfiles div img {
        width: 8vw;
        height: 8vw;
        object-fit: cover;
        border-radius: 100%;
        cursor: pointer;
    }

    .currentProfile {
        border-left: solid 10px #e63946!important;
    }

    .about {
        width: 45vw;
        background-color: #e63946;
        padding: 20px;
    }

    .moreAbout {
        width: 45vw;
        background-color: #457b9d;
        color: white;
        padding: 20px;
    }

    .photoSection {
        padding: 2vw 3vw 3vw 3vw;
        background-color: #457b9d;
    }

    .photoSection h3 {
        font-size: 50px;
        margin: 0;
        text-align: center;
        color: #f1faee;
        letter-spacing: 2vw;
        margin-bottom: 2vw;
    }

    .photos {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }

    .photos img {
        width: 25em;
        height: 15em;
        object-fit: cover;
    }
</style>