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
        <div>
            <div class="banner">
                <h1>
                -- Content goes here --
                </h1>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderApp',

    data(){
        return{
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
                
            ]
        }
    }
}
</script>

<style lang="scss">
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
            padding: 3rem;
            font-size: small;
            
        }
    }
</style>