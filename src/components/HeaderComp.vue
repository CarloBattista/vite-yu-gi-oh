<template>
    <div>
        <div class="header">
            <a href="/">
                <img class="logo" src="/_resources/yugioh_logo.svg" alt="logo yu-gi-oh">
                <span class="heading">Yu-Gi-Oh Api</span>
            </a>
        </div>
    </div>
</template>

<script>
    export default {
        name: "HeaderComp",
    }
</script>

<style lang="scss" scoped>
.header{
    position: sticky;
    z-index: 999;
    width: 100%;
    height: 70px;
    padding: 0 60px;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    background: #fff;
    a{
        display: flex;
        align-items: center;
        .logo{
            width: 90px;
            margin-right: 2em;
        }
        .heading{
            color: #000;
            font-size: 1.5rem;
            font-weight: 700;
        }
    }
}
</style>