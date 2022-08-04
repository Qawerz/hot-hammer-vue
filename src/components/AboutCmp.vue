<template>
    <div id="about">
        <BgImageCmp/>
        <h1>About</h1>
    </div>
</template>

<script>
import BgImageCmp from "@/components/BgImageCmp"
export default {
    components:{
        BgImageCmp
    }
}
</script>

<style lang="scss" scoped>
#about {
    filter: brightness(100%);
    height: 100vh;
}
</style>