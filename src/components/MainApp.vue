<template >
    <main>
        <section>
            <div>
                <h3>
                    DC COMICS
                </h3>

                <ul>
                    <li v-for="link in MainLinks">
                       <a href="">{{ link.text }}</a> 
                    </li>
                </ul>
            </div>
        </section>
    </main>
</template>

<script>
export default {
    name: 'MainApp',

    data(){
        return{
            MainLinks:[
                {
                    text: 'characters',
                },
                {
                    text: 'comics',
                },
                {
                    text: 'movies',
                },
                {
                    text: 'TV',
                },
                {
                    text: 'Games',
                },
                {
                    text: 'Videos',
                },
                {
                    text: 'News',
                },
            ]
        }
    }
}
</script>

<style lang="scss">
    @use '../style/partials/variables' as *;
    @use '../style/partials/mixins' as *;

    main{
        background-image:url('../assets/img/footer-bg.jpg') ;

        section{
            @include container;
            padding: 2rem 1rem;
        }
    }

    h3{
        color:$textWhite;
        margin-bottom: .8rem;
    }
    li{
        font-size: 0.8rem;
        a{
            color: $textWhite;
            text-decoration: none;
        }
    }

</style>