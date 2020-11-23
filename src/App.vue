`<template>
    <div class="main">
        <WrapText/>
        <div class="container">
            <div class="wrap">
                <ContentBlock/>
                <ScrollBlocks/>
            </div>
        </div>
    </div>
</template>

<script>
import ScrollBlocks from "@/components/ScrollBlocks";
import WrapText from "@/components/WrapText";
import ContentBlock from "@/components/ContentBlock";

export default {
    name: 'App',
    components: {
        ScrollBlocks,
        WrapText,
        ContentBlock
    }
}
</script>

<style scoped>
.main {
    height: 90vh;
    width: 100%;
}

.container {
    display: flex;
    flex-direction: column;

    height: 100%;
}

.wrap {
    position: relative;
    height: 100%;
    display: flex;
    flex-direction: column;
}
</style>
`