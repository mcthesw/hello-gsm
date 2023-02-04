<script setup lang="ts">
function openDownloadPage() {
    window.open('https://github.com/mcthesw/game-save-manager/releases');
}
</script>

<template>
    <div class="download-buttons">
        <div class="primary-buttons">
            <button type="button" id="download-btn" @click="openDownloadPage">
                下载最新版本
                <small>Windows 稳定版本</small>
            </button>
            <ElPopover trigger="click" placement="bottom-end">
                <template #reference>
                    <button type="button" id="show-more-btn"><i class="fa-solid fa-angle-down"></i></button>
                </template>
                <a href="https://github.com/mcthesw/game-save-manager/actions">
                    Linux(预览版本)<br/>MacOS(预览版本)<br/>Win(预览版本)
                </a>
            </ElPopover>
        </div>
        <p class="terms">本软件使用<a href="https://github.com/mcthesw/game-save-manager/blob/master/LICENSE">GPLv2</a>协议进行授权
        </p>
    </div>
</template>

<style lang="stylus">
.download-buttons a
    color gray
    &:hover
        color #00ADB5

.primary-buttons
    display flex
    align-content center
    justify-content center
    &>button
        height 60px
    & small
        display block
#download-btn
    width 200px
    background-color #1e88e5
    color #fff
    border none
    font-size 20px
    font-weight 500
    margin-right 3px
    &:hover
        background-color #1976d2
#show-more-btn
    width 40px
    background-color #1e88e5
    color #fff
    border none
    font-size 20px
    font-weight 500
    margin-right 3px
    &:hover
        background-color #1976d2
</style>
