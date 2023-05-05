<template>
    <div>
        <div class="container_selector">
            <div class="w-80">
                <div class="sl_container">
                    <select class="select_type" name="selectType" id="">
                        <option value="0" selected>Alien</option>
                    </select>
                    <div class="icon_arrow">
                        <i class="fa-solid fa-caret-down"></i>
                    </div>
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
        position: relative;
        display: inline-block;
        .select_type{
            position: relative;
            appearance: none;
            width: 200px;
            height: 42px;
            padding: 8px 25px;
            border-radius: 4px;
            font-size: 1rem;
            font-weight: 500;
            outline: none;
            cursor: pointer;
        }
        .icon_arrow{
            position: absolute;
            top: 0;
            right: 0;
            width: 42px;
            height: 100%;
            text-align: center;
            display: flex;
            align-items: center;
            justify-content: center;
            .fa-caret-down{
                color: #000;
                font-size: 1rem;
            }
        }
    }
}
</style>