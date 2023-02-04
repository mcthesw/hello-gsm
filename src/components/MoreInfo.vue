<script setup lang="ts">
let info = [
    { name: '广受好评', icon: 'fa-regular fa-thumbs-up', link: '#liked' },
    { name: '使用教程', icon: 'fa-solid fa-sliders', link: '#how2use' },
    { name: '开放合作', icon: 'fa-regular fa-comment', link: '#open' },
    { name: '关于作者', icon: 'fa-regular fa-address-card', link: '#about' }
]
</script>

<template>
    <div class="info-menu">
        <a class="info-menu-item no-underline" v-for="item in info" :key="item.name" :href="item.link">
            <div class="info-menu-item-icon">
                <i :class="item.icon"></i>
            </div>
            <div class="info-menu-item-name">
                {{ item.name }}
            </div>
        </a>
    </div>
    <div class="detail-info-list">
        <ElRow class="detail-info" id="liked" :gutter="20">
            <ElCol :xs="24" :sm="24" :md="6" :lg="6" :xl="6">
                <img src="../assets/pic1.png"/>
            </ElCol>
            <ElCol :xs="24" :sm="24" :md="18" :lg="18" :xl="18">
                <h1>受玩家喜爱</h1>
                <p>游戏存档管理器最先在bilibili和小黑盒上发布，收到了很多玩家的反馈，我很开心这个工具能给大家提供帮助，它也会在未来不断更新，添加有用的功能</p>
            </ElCol>
        </ElRow>
        <ElRow class="detail-info" id="how2use" :gutter="20">
            <ElCol :xs="24" :sm="24" :md="18" :lg="18" :xl="18">
                <h1>使用教程</h1>
                <p>该软件功能明了，直接上手也可以使用，不过，在以下链接中，也有各种入门教程</p>
                <p> <i class="fa-brands fa-youtube"></i>&nbsp
                    <a href="https://www.bilibili.com/video/BV1Zu411q7W1/">

                        Bilibili上的视频教程
                    </a>
                </p>
                <p>
                    <i class="fa-regular fa-file-lines"></i>&nbsp&nbsp
                    <a href="https://www.bilibili.com/read/cv15774558">
                        Bilibili上的文字教程
                    </a>
                </p>
            </ElCol>
            <ElCol :xs="24" :sm="24" :md="6" :lg="6" :xl="6">
                <img src="../assets/pic2.png"/>
            </ElCol>
        </ElRow>
        <ElRow class="detail-info" id="open" :gutter="20">
            <ElCol :xs="24" :sm="24" :md="6" :lg="6" :xl="6">
                <img src="../assets/pic3.png"/>
            </ElCol>
            <ElCol :xs="24" :sm="24" :md="18" :lg="18" :xl="18">
                <h1>提出问题，解决它</h1>
                <p>你可以在 <a href="https://github.com/mcthesw/game-save-manager/issues">Github Issue</a>、<a
                        href="https://space.bilibili.com/4087637">Bilibili 评论区</a>提出建议或者提交 Bug，我会定期检查</p>
                <p>如果可能，我会尽快处理它们</p>
                <p>如果你也愿意参加开发，那太好了，请不要吝啬你的<a href="https://github.com/mcthesw/game-save-manager/pulls">Pull Request</a>
                </p>
            </ElCol>
        </ElRow>
        <ElRow class="detail-info" id="about" :gutter="20">
            <ElCol :xs="24" :sm="24" :md="12" :lg="12" :xl="12">
                <el-card :body-style="{ padding: '0px' }">
                    <img src="../assets/my-slime.png" class="my-avatar" />
                    <div style="padding: 14px">
                        <span>Sworld</span>
                        <div class="bottom">
                            <time class="time"></time>
                            <el-button text class="button">我是一个开发者，也是一个玩家</el-button>
                        </div>
                    </div>
                </el-card>
            </ElCol>
            <ElCol :xs="24" :sm="24" :md="12" :lg="12" :xl="12">
                <h1>关于我</h1>
                <p>编程语言：Typescript, Python, Rust, C#</p>
                <p>常用框架：Vue3, Element-plus, FastAPI, Express</p>
                <p>我的博客：<a href="http://blog.sworld.club/">blog.sworld.club</a></p>
                <p>代表作品：<a href="https://github.com/mcthesw/game-save-manager">存档管理器</a>, <a
                        href="https://github.com/mcthesw/tomato-clock.js">番茄钟</a></p>
            </ElCol>
        </ElRow>
    </div>
</template>

<style lang="stylus">
a
    text-decoration underline
    color inherit
    &:hover
        color #00ADB5
.no-underline
    text-decoration none
.info-menu
    display flex
    justify-content space-evenly
    padding-left 20%
    padding-right 20%
    flex-wrap wrap;
    margin-top 20px
    margin-bottom 20px
    &>.info-menu-item
        padding 10px
        height 120px
        width 20%
        min-width 150px
        &:hover
            background-color #EEEEEE
        &>.info-menu-item-icon
            font-size 50px
            text-align center
            margin-bottom 10px
        &>.info-menu-item-name
            margin-top 20px
            text-align center
            font-size 20px
.detail-info
    padding 50px
    padding-left 20%
    padding-right 20%
    font-size 20px
    &:nth-child(odd)
        background-color #EEEEEE
    &:nth-child(even)
        background-color #FFFFFF
.my-avatar,img
    width 100%
    height auto
</style>
