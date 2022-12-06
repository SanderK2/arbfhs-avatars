<template>
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
    
    <div>
        <h2>{{profileObject.ingress}}</h2>
                <p>{{profileObject.aboutMe}}</p>
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

    .header-image {
        position: absolute;
        z-index: -1;
        width: 100vw;
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
</style>