<script setup lang="ts">
import { ref, watch } from 'vue';

const screen_width = ref(document.body.clientWidth);
const is_vertical_page = ref(screen_width.value < 720);

window.addEventListener('resize', () => {
    const screenWidths = document.body.clientWidth;
    screen_width.value = screenWidths;
});

watch(screen_width, (newVal, _) => {
    is_vertical_page.value = newVal < 720;
});
</script>

<template>
    <nav class="top-nav-wide" v-if="!is_vertical_page">
        <ul>
            <li><img src="../assets/electron.jpg" alt="icon" /></li>
            <li><a href="">游戏存档管理器</a></li>

            <li class="flex-grow"></li>

            <li>
                <a href="https://help.sworld.club"><i class="fas fa-question-circle" />
                    &nbsp使用教程
                </a>
            </li>
            <li>
                <a href="https://github.com/mcthesw/game-save-manager">
                    <i class="fa-brands fa-github" />
                    &nbspGithub
                </a>
            </li>
            <li>
                <a href="https://gitee.com/sworldS/game-save-manager">
                    <i class="fa-solid fa-code-branch" />
                    &nbspGitee
                </a>
            </li>
            <li><a href="https://afdian.net/a/Sworld">
                    <i class="fa-solid fa-bolt" />
                    &nbsp爱发电
                </a>
            </li>
        </ul>
    </nav>
    <!-- 竖屏狭窄设备的nav -->
    <div class="top-nav-narrow" v-else>
        <ElRow justify="space-evenly">
            <ElCol :span="5">
                <ElLink href="https://help.sworld.club"><i class="fas fa-question-circle" />
                    &nbsp使用教程
                </ElLink>
            </ElCol>
            <ElCol :span="5">
                <ElLink href="https://github.com/mcthesw/game-save-manager">
                    <i class="fa-brands fa-github" />
                    &nbspGithub
                </ElLink>
            </ElCol>
            <ElCol :span="5">
                <ElLink href="https://gitee.com/sworldS/game-save-manager">
                    <i class="fa-solid fa-code-branch" />
                    &nbspGitee
                </ElLink>
            </ElCol>
            <ElCol :span="5">
                <ElLink href="https://afdian.net/a/Sworld">
                    <i class="fa-solid fa-bolt" />
                    &nbsp爱发电
                </ElLink>
            </ElCol>
        </ElRow>
    </div>
</template>

<style lang="stylus">
.top-nav-wide a
    color #fff
    text-decoration none
    &:hover
        color #00ADB5
        text-decoration none
.flex-grow
    flex-grow 1
.top-nav-wide 
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
.top-nav-narrow
    padding-top 10px
    padding-bottom 10px
    background-color #222831
.el-link
    color white
</style>