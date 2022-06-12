<template>
    <div id="app">
        <router-view/>
        <FooterGuite v-show="$route.meta.showFooter"/>
    </div>
</template>

<script>
    import FooterGuite from "@/components/FooterGuite/FooterGuite";
    export default {
        name: "App",
        components: {FooterGuite}
    }
</script>

<style lang="less">
</style>