<template>
    <div class="main">
        <visual-slide></visual-slide>
    </div>
</template>

<script>
    export default {
        name:'Main',
        components: {
            VisualSlide: () => import("@/components/main/VisualSlide.vue")
         }
    }
</script>

<style lang="scss" scoped>

</style>