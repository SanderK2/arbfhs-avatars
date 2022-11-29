<template>
    <button @class="ComputedClass" />
</template>

<script>
export default {
    name: "Button",
    props: {
        rounded: {
            type: Boolean,
            required: False,
            default: False
        },
        light: {
            type: Boolean,
            required: False,
            default: False
        },
        color: {
            type: String,
            required: False,
            default: ""
        }
    },
    computed: {
        ComputedClass() {
            return ``
        }
    }
}
</script>

<style scoped>

button {
    margin: 7px;
    border-radius: 3px;
    outline: none;
    border: 1.5px;
}

rounded {
    border-radius: 100%;
}

danger {
    background: red;
}


danger-light {
    background: rgb(255, 113, 113);
}

primary {
    background: rgb(22, 181, 255);
}

primary-light {
    background: rgb(165, 226, 255);
}

success {
    background: rgb(125, 255, 39);
}

success-light {
    background: rgb(196, 255, 157);
}

info {
    background: rgb(100, 100, 100);
}

info-light {
    background: rgb(214, 214, 214);
}

warning {
    background: rgb(255, 166, 0);
}

warning-light {
    background: rgb(255, 208, 121);
}
</style>