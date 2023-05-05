<template>
    <div>
        <div class="container_selector">
            <div class="w-80">
                <div class="sl_container">
                    <select class="select_type" name="selectType" id="">
                        <option value="0" selected>Alien</option>
                    </select>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "TypeSelector",
    }
</script>

<style lang="scss" scoped>
.container_selector{
    widows: 100%;
    padding: 60px 0;
    .sl_container{
        display: flex;
        align-items: center;
        .select_type{
            width: 15%;
            padding: 8px 25px;
            border-radius: 4px;
            font-size: 1rem;
            font-weight: 500;
            outline: none;
            cursor: pointer;
        }
    }
}
</style>