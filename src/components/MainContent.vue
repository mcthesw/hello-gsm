<script setup lang="ts">
import DownloadArea from './DownloadArea.vue'
</script>

<template>

    <ElRow :gutter="10" class="container">
        <el-col :xs="24" :sm="24" :md="8" :lg="8" :xl="8">
            <div class="grid-content">
                <h1>
                    存档管理
                    <br/>
                    我来代你操作
                </h1>
                <p>舒适的使用体验 不收取费用 开放源代码 活跃的社区</p>
                <DownloadArea />
            </div>
        </el-col>
        <el-col :xs="24" :sm="24" :md="16" :lg="16" :xl="16">
            <div class="grid-content">
                <img src="gsm-main-ui.png" alt="screenshot of game-save-manager" />
            </div>
        </el-col>
    </ElRow>

</template>

<style lang="stylus">     
.el-row
    margin-right 0 !important // why this is -5px ?
.container
    margin-bottom: 20px;
    display: flex;
    flex-wrap: wrap
    padding-left 10%
    padding-right 10%
    padding-top 30px
    padding-bottom 30px
    background-color #393E46
    text-align center
    &>.el-col
        padding-top 10px
        padding-bottom 10px
        padding-left 10px
        padding-right 10px
        &>.grid-content
            height 100%
            &>h1 p
                padding-top 10px
                padding-bottom 10px
            &>img
                border-radius 10px
                width: auto
                height: auto
                max-width: 100%
                max-height: 100%
    & h1
        font-size 40px
        font-weight 600
        margin 0
        margin-top 20px
        line-height 1.3
        color white
    & p
        color gray
        margin-top 20px
        margin-bottom 20px
</style>
