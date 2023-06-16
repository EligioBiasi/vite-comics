<template>
     <article>
        <div class="card">
            <img :src="ComicImage" alt="ComicTitle">
        </div>
        <p>
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
        div.card{
            width: 100%;
        }
        img{
            display: block;
            width: 100%;
            height: 250px;
        }
    }
</style>