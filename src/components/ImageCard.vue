<template>
     <article>
        <div class="picture">
            <img :src="ComicImage" alt="#">
        </div>
        <p class="cooking-time">
            {{ComicTitle}}
        </p>
    </article>
</template>
<script>

export default {
    props:{
        ComicImage: String,
        ComicTitle: String,
    }
}
</script>
<style lang="scss" scoped>
    article{
        width: calc((100% / 6));

        img{
            width: 100%;
        }
    }
</style>