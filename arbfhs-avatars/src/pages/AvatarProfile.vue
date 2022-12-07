<template>
    <div class="mainProfile">
        <div class="profile">
    <div>
        <div>

        </div>
        <img class="header-image" :src="profileObject.profileImg" alt="">
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
            Lorem ipsizzle fo the bizzle amizzle, consectetuer adipiscing ma nizzle. Fizzle velizzle, dang volutpizzle, suscipizzle quis, gravida vizzle, arcu. Pellentesque fo shizzle tortor. Sed fo shizzle. Stuff izzle doggy dapibizzle turpis tempizzle nizzle. Maurizzle pellentesque phat et turpis. izzle tortor. Pellentesque eleifend rhoncizzle mofo. hac phat platea yippiyo. Bizzle dapibus. Sizzle dope rizzle, pretium the bizzle, fo shizzle ac, eleifend vitae, boom shackalack. Gangster suscipit. Integer sempizzle velizzle sizzle own yo'.
        </div>
    </div>
    </div>
    <div class="otherProfiles">
        <div class="profileCircle currentProfile">
            <img :src="profileObject.profileImg" alt="">
        </div>
        <div class="profileCircle">
            <img :src="profileObject.profileImg" alt="">
        </div>
        <div class="profileCircle">
            <img :src="profileObject.profileImg" alt="">
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
    setup() {
        
    },
}
</script>

<style>
    .blergh {
        padding-top: 9em;
        height: 15em;
        width: 100vw;
        display: flex;
        align-items: flex-end;
        color: white;
    }

    .blergh div {
        margin-left: -1.5em;
    }

    h1 {
        margin: 0;
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
        background-color: #264653;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .profileCircle img {
        width: 8vw;
        height: 8vw;
        object-fit: cover;
        border-radius: 100%;
        cursor: pointer;
    }

    .currentProfile img {
        border: solid 3px #2a9d8f;
    }

    .about {
        width: 45vw;
        background-color: #e76f51;
        padding: 20px;
    }

    .moreAbout {
        width: 45vw;
        background-color: #264653;
        color: white;
        padding: 20px;
    }
</style>