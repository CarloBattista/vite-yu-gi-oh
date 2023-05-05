<script>
import { store } from "../store"

export default {
    name: "CardGame",
    props: ["detailsCard"],

    data() {
        return {
            store
        }
    },
}
</script>

<template>
    <div class="card" v-if="store.arrayCards.length > 0" v-for="(element, index) in store.arrayCards">
        <div class="imageWrap">
            <img class="imageCard" :src="element.card_images[0].image_url" alt="image">
        </div>
        <div class="infoCard">
            <h2 class="nameCard">{{ element.name }}</h2>
            <h3 class="typeCard">{{ element.type }}</h3>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.card {
    width: 100%;
    background: rgb(191, 1, 1);

    .imageWrap {
        width: 100%;
        height: auto;

        .imageCard {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }

    .infoCard {
        padding: 20px;

        .nameCard {
            color: #fff;
            font-size: 1rem;
            font-weight: 700;
        }

        .typeCard {
            color: #fff;
            font-size: .8rem;
            font-weight: 400;
        }
    }
}</style>