<template>
     <article>
        <div class="picture">
            <img :src="ComicElement.thumb" alt="#">
        </div>
        <p class="cooking-time">
            {{ComicElement.series}}
        </p>
    </article>
</template>
<script>

export default {
    props:{
        ComicElement: Object
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