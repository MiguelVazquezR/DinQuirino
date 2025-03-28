<template>
    <img v-if="color == 'white'" src="@/../../public/images/logo_white.png" class="select-none" :draggable="false" alt="Logo con un agabe y el texto 'Don Quirino'" />
    <img v-else src="@/../../public/images/logo.png" class="select-none" :draggable="false" alt="Logo con un agabe y el texto 'Don Quirino'" />
</template>
<script>

export default {
    props: {
        color: {
            type: String,
            default: "black",
        },
    },
}
</script>
