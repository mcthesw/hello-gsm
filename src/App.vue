<script setup lang="ts">
import NavBar from './components/NavBar.vue'
import MainContent from './components/MainContent.vue'
import MoreInfo from './components/MoreInfo.vue'
import FooterArea from './components/FooterArea.vue';
</script>

<template>
    <NavBar />
    <MainContent />
    <ElBacktop :right="100" :bottom="100" />
    <MoreInfo />
    <FooterArea/>
</template>

<style lang="stylus">
font-size = 14px
title-size = 20px
body
    margin 0
    padding 0
</style>
