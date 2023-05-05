<template>
    <div>
        <div class="card">
            <div class="imageWrap">
                <img class="imageCard" src="https://static0.srcdn.com/wordpress/wp-content/uploads/2020/04/dprpen025-57948.1473911460.jpg" alt="image">
            </div>
            <div class="infoCard">
                <h2 class="nameCard">Name Card</h2>
                <h3 class="typeCard">Type</h3>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "CardGame",
}
</script>

<style lang="scss" scoped>
.card{
    width: 100%;
    background: rgb(191, 1, 1);
    .imageWrap{
        width: 100%;
        height: auto;
        .imageCard{
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    .infoCard{
        padding: 20px;
        .nameCard{
            color: #fff;
            font-size: 1rem;
            font-weight: 700;
        }
        .typeCard{
            color: #fff;
            font-size: .8rem;
            font-weight: 400;
        }
    }
}
</style>