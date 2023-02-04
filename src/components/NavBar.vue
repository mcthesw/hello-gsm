<script setup lang="ts">

</script>

<template>
    <nav class="top-nav">
        <ul>
            <li><img src="../assets/electron.jpg" alt="icon"/></li>
            <li><a href="">游戏存档管理器</a></li>
            <li>在线尝试（未完工）</li>
            <li class="flex-grow"></li>
            <li><a href="https://github.com/mcthesw/game-save-manager"><i class="fa-brands fa-github"></i>&nbspGithub</a></li>
            <li><a href="https://gitee.com/sworldS/game-save-manager"><i class="fa-solid fa-code-branch"></i>&nbspGitee</a></li>
            <li><a href="https://afdian.net/a/Sworld"><i class="fa-solid fa-bolt"></i>&nbsp爱发电</a></li>
        </ul>
    </nav>
</template>

<style lang="stylus">
.top-nav a
    color #fff
    text-decoration none
    &:hover
        color #00ADB5
        text-decoration none
.flex-grow
    flex-grow 1
.top-nav 
    & > ul
        display flex
        list-style-type none
        padding 0 80px 0 80px
        margin 0
        height 50px
        background-color #222831
        color #EEEEEE
        font-size 14px
        font-weight 600
        line-height 50px
        align-items center
        justify-content space-between
        li
            display flex
            align-items center
            justify-content center
            padding 0 10px
        img
            height 30px
            width 30px
            border-radius 50%
            object-fit scale-down
</style>