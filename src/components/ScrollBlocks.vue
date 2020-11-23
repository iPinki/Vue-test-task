<template>
    <div class="bottom">
        <div
            class="scroll"
            v-bind:class="[isTopActive ? 'active' : '']"
        >
            <TopScroll
                :isTopActive="isTopActive"
                @topChange="topToggleClass"
            />
        </div>
        <div
            class="scroll"
            v-bind:class="[isBottomActive ? 'active' : '']"
        >
            <BottomScroll
                :isBottomActive="isBottomActive"
                @bottomChange="bottomToggleClass"
            />
        </div>
    </div>
</template>

<script>
import TopScroll from "@/components/TopScroll";
import BottomScroll from "@/components/BottomScroll";

export default {
    name: "ScrollBlocks",
    components: {
        TopScroll,
        BottomScroll
    },
    data() {
        return {
            isTopActive: false,
            isBottomActive: false
        }
    },
    methods: {
        topToggleClass: function () {
            this.isTopActive = !this.isTopActive
        },
        bottomToggleClass: function () {
            this.isBottomActive = !this.isBottomActive
        }
    }
}
</script>

<style scoped>
.bottom {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    position: absolute;
    height: 100%;
    bottom: 0;

}

.scroll {
    height: 10vh;

    overflow-x: hidden;
    overflow-y: scroll;

    background-color: #fff;

    transition: 1s;
}

.active {
    height: 90%;
}
</style>