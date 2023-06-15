<template >
    <header>
        <div>
            <nav>
                <img src="../assets/img/dc-logo.png" alt="DC comics logo">
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    
}
</script>

<style lang="scss">
    @use '../style/partials/variables' as *;
    @use '../style/partials/mixins' as *;

    header{
        background-color: black;
        padding-top: 2.5rem;

        div{
            background-color: white;
        }

        nav{
            @include container;
            padding: 1rem;

            img{
                width: 80px;
            }
        }
    }
</style>