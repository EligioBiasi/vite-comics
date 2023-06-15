<template >
    <footer>
        <div class="footer-bg">
            <div class="container">
                <div>
                    <button>
                        sign up now
                    </button>
                </div>

                <div class="footer-right">
                    <h2>
                        follow us
                    </h2>
                    <ul>
                        <li>
                            <img src="../assets/img/footer-facebook.png" alt="">
                        </li>
                        <li>
                            <img src="../assets/img/footer-periscope.png" alt="">
                        </li>
                        <li>
                            <img src="src/assets/img/footer-twitter.png" alt="">
                        </li>
                        <li>
                            <img src="src/assets/img/footer-youtube.png" alt="">
                        </li>
                        <li>
                            <img src="src/assets/img/footer-pinterest.png" alt="">
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    data(){
        return{

        }
    }
}
</script>

<style lang="scss" scoped>
    @use '../style/partials/variables' as *;
    @use '../style/partials/mixins' as *;

    div.footer-bg{
        color:$BackgroundGray;
        padding: 3rem 0;
    }

    div.container{
        @include container;
        @include flex(row,space-between);
        div{
            padding:0 1rem;
        }
    }
    
    button{
        border: 3px solid #1361aa;
        text-transform: uppercase;
        background-color: $BackgroundGray;
        color: $textWhite;
        padding: .7rem;
    }

    h2{
        text-transform: uppercase;
        font-size: large;
        color: #1361aa;
    }

    div.footer-right,
    ul{
        @include flex;
    }

    li{
        padding: 0 .5rem;
    }
</style>