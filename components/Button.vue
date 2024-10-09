<template>
    <button class="button" :style="{ backgroundColor: buttonColor}"> Enroll Now </button>
</template>

<script>
export default {
    props: {
        buttonColor: {
            type: String,
            default: 'rgba(50, 113, 210, 1)',
        }
    }
}
</script>

<style lang="scss" scoped>
.button {
    width: 164px;
    height: 46px;
    border-radius: 4px;
    border: none;
    color: $blockcolor;
    font-size: 18px;
    font-weight: 700;
}
</style>