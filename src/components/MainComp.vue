<template>
    <div>
        <div class="container_main">
            <div class="w-80" id="different_style">
                <div class="container_heading">
                    <span class="cards_found_count">Found <span class="found_number">00</span> cards</span>
                </div>
                <div class="container_cards">
                    <CardGame />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import CardGame from "./CardGame.vue"

export default {
    name: "MainComp",
    components: {
        CardGame,
    },
}
</script>

<style lang="scss" scoped>
.container_main {
    width: 100%;

    #different_style {
        background: #fff;
        padding: 60px 40px;
    }

    .container_heading {
        widows: 100%;
        height: 70px;
        padding: 0 30px;
        display: flex;
        align-items: center;
        background: #121212;

        .cards_found_count {
            color: #fff;
            font-size: 1rem;
            font-weight: 400;

            .found_number {
                font-weight: 700;
            }
        }
    }

    .container_cards {
        width: 100%;
        padding: 1em 0;
        display: grid;
        gap: 1em;
        grid-template-columns: repeat(5, 1fr);
        text-align: center;
    }
}</style>