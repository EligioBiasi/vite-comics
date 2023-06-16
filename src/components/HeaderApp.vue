<template >
    <header>
        <div class="white-background">
            <nav>
                <div>
                    <img src="../assets/img/dc-logo.png" alt="DC comics logo">
                </div>
                <div>
                    <ul>
                        <li v-for="link in NavContainerLinks">
                            <a href="#">{{ link.text.toUpperCase() }}</a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
        <div class="jumbotron">
        </div>
        <div>
            <div class="banner">
                <ImageCard v-for="Comic in ComicsForCard"
                :ComicImage="Comic.thumb"
                :ComicTitle="Comic.series"/>
            </div>
        </div>
    </header>
</template>

<script>
import ImageCard from './ImageCard.vue'
export default {
    name: 'HeaderApp',
    
    data(){
        return{
            components:{
                ImageCard,
            },
            NavContainerLinks:[
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
                    text: 'tv',
                },
                {
                    text: 'Games',
                },
                {
                    text: 'collectibles',
                },
                {
                    text: 'videos',
                },
                {
                    text: 'fans',
                },
                {
                    text: 'news',
                },
                {
                    text: 'shop',
                },
                
            ],
            ComicsForCard:[
                {
                    thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book",
                },
                {
                    thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book",
                },
                {
                    thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel",
                },
                {
                    thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book",
                },
                {
                    thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel",
                },
                ],
            
        }
    }
}
</script>

<style lang="scss" scoped>
    @use '../style/partials/variables' as *;
    @use '../style/partials/mixins' as *;
    header{
        background-color: $textBlack;
        padding-top: 2.5rem;

        nav{
            @include container;
            @include flex(row,space-between);
            padding: 1rem;
        }

        div.white-background{
            background-color: white;
            img{
                width: 80px;
            }
        }

        ul{
            @include flex();
            
            a{
                text-decoration: none;
                color: $textGray;
                font-size: small;
                font-weight: bold;
            }

            li{
                @include flex();
                padding: 0.45rem;

                :hover{
                    color: #0282f9;
                    border-bottom:#0282f9 solid 2px;
                }
            }
        }

        div.banner{
            @include container;
            color:$textWhite;
            padding: 3rem 0;
        }
    }

    div.jumbotron{
        background-image: url('../assets/img/jumbotron.jpg');
        background-size: cover;
        background-position: top;
        width: 100vw;
        height: 300px;
    }
</style>