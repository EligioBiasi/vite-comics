<template >
    <main>
        <section>
            <div class="list-contanier">
                <div class="list">
                    <h3>
                        dc comics
                    </h3>

                    <ul>
                        <li v-for="link in ComicLinks">
                        <a href="">{{ link.text }}</a> 
                        </li>
                    </ul>
                </div>
                <div class="list">
                    <h3>
                        shop
                    </h3>

                    <ul>
                        <li v-for="link in ShopLinks">
                            <a href="">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="list-contanier">
                <div>
                    <h3>
                        dc
                    </h3>

                    <ul>
                        <li v-for="link in DcLinks">
                            <a href="">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="list-contanier">
                <div>
                    <h3>
                        sites
                    </h3>

                    <ul>
                        <li v-for="link in SitesLinks">
                            <a href="">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </section>

        <img src="../assets/img/dc-logo-bg.png" alt="dc-logo-big">

    </main>
</template>

<script>
export default {
    name: 'MainApp',

    data(){
        return{
            ComicLinks:[
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
            ],

            ShopLinks:[
                {
                    text: 'shop DC',
                },
                {
                    text: 'Shop DC Collectibles',
                },
            ],

            DcLinks:[
                {
                    text: 'Terms of Use',
                },
                {
                    text: 'Privacy policy (New)',
                },
                {
                    text: 'Ad Choices',
                },
                {
                    text: 'Advertising',
                },
                {
                    text: 'Jobs',
                },
                {
                    text: 'Subscriptions',
                },
                {
                    text: 'Talent Workshops',
                },
                {
                    text: 'CPSC Certificates',
                },
                {
                    text: 'Ratings',
                },
                {
                    text: 'Shop Help',
                },
                {
                    text: 'Contact Us',
                },
            ],

            SitesLinks:[
                {
                    text: 'DC',
                },
                {
                    text: 'MAD Magazine',
                },
                {
                    text: 'DC Kids',
                },
                {
                    text: 'DC Universe',
                },
                {
                    text: 'DC Power Visa',
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
    @use '../style/partials/variables' as *;
    @use '../style/partials/mixins' as *;

    main{
        background-image:url('../assets/img/footer-bg.jpg') ;
        position: relative;
        z-index: -1;

        section{
            @include container;
            @include flex(row,start,start);
            padding: 2rem 1rem;

            div.list{
                margin-bottom: 1rem;
            }

            div.list-contanier{
                padding-right:1rem;
            }
        }
    }

    h3{
        color:$textWhite;
        margin-bottom: .8rem;
        text-transform: uppercase;
    }

    li{
        font-size: 0.8rem;
        font-weight: lighter;
        padding: .2rem 0;
        a{
            color: gray;
            text-decoration: none;
        }
    }

    img{
        position: absolute;
        right: 15%;
        top:-20%;
        width: 25%;
    }
</style>