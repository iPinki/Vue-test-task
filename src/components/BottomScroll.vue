<template>
    <div class="sbt">
        <div class="bottom-flex">
            <h1>BOTTOM</h1>
            <div
                class="circle-plus closed"
                v-bind:class="[isBottomActive ? 'opened': 'closed']"
                @click="toggleClass()"
            >
                <div class="circle">
                    <div class="horizontal"></div>
                    <div class="vertical"></div>
                </div>
            </div>
        </div>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cum quia, repellat! Aspernatur
            dicta
            eum
            facilis, suscipit totam voluptates! Ad aliquam aut dolorum facere, ipsa magni minus
            neque
            quas
            quis
            quos sed tempora veniam voluptatum. Beatae consequuntur corporis cum dicta, doloremque
            enim
            esse
            ex
            hic id impedit inventore minima natus nesciunt possimus quibusdam quos recusandae sit
            sunt
            ullam
            voluptates. A ad aliquid animi aperiam asperiores assumenda blanditiis consectetur
            cumque
            delectus,
            dicta dolore dolorum error est eum eveniet fugiat harum illum ipsam iste itaque labore
            maxime
            molestias nam nemo nesciunt nisi officia omnis possimus, praesentium quis quisquam quo
            similique
            sint soluta tempore unde voluptatem? Aliquid consequatur cupiditate doloribus dolorum
            exercitationem, facilis, impedit in inventore iure libero magnam, nostrum numquam
            perspiciatis
            placeat quasi quia quidem repellendus tempore unde vero! Culpa illo laboriosam
            praesentium
            repellendus velit? Aliquam asperiores atque doloribus ex excepturi impedit mollitia
            nesciunt
            perspiciatis, reiciendis sequi sint sit tempora, tempore vitae voluptatum!
        </p>
    </div>
</template>

<script>
export default {
    name: "BottomScroll",
    props: {
        isBottomActive: Boolean
    },
    methods: {
        toggleClass: function () {
            this.$emit('bottomChange')
        }
    }
}
</script>

<style scoped>
.active {
    height: 90%;
}

.sbt {
    padding: 15px;

    border-top: 1px solid #ccc;
}

.bottom-flex {
    display: flex;
    justify-content: space-between;
}

.closed .vertical {
    transition: all .5s ease-in-out;
    transform: rotate(-90deg);
}

.closed .horizontal {
    transition: all .5s ease-in-out;
    transform: rotate(-90deg);
    opacity: 1;
}

.opened {
    opacity: 1;
}

.opened .vertical {
    transition: all .5s ease-in-out;
    transform: rotate(90deg);
}

.opened .horizontal {
    transition: all .5s ease-in-out;
    transform: rotate(90deg);
    opacity: 0;
}

.circle-plus {
    margin: 7px 7px 0 0;
    height: 20px;
    width: 20px;
    font-size: 10px;
    opacity: .7;
}

.circle-plus .circle {
    position: relative;
    width: 25px;
    height: 25px;
}

.circle-plus .circle .horizontal {
    position: absolute;
    background-color: #000;
    width: 20px;
    height: 3px;
    left: 50%;
    margin-left: -12px;
    top: 50%;
    margin-top: -6px;
}

.circle-plus .circle .vertical {
    position: absolute;
    background-color: #000;
    width: 3px;
    height: 20px;
    left: 50%;
    margin-left: -2.5px;
    top: 50%;
    margin-top: -15px;
}
</style>