<template>
    <div class="content">
        <div class="top">
            <div class="header">
                <img class="logo" src="../assets/header-logo.jpg" alt="logo">
                <h1 class="title">Start treatment early for your patients with mCSPC</h1>
            </div>
            <Cards/>
        </div>
    </div>
</template>

<script>
import Cards from "@/components/Cards";

export default {
    name: "Content",
    components: {
        Cards
    }
}
</script>

<style scoped>
.content {
    position: relative;
    display: flex;
    flex-direction: column;

    height: 100%;

    background-color: #fff;
}

.top {
    display: flex;
    flex-direction: column;

    width: 100%;
    height: 100%;
}

.header {
    display: flex;
    justify-content: flex-start;

    padding: 40px 25px;
}

.logo {
    width: 130px;
    height: 47px;
}

.title {
    margin-left: 20%;

    font-size: 42px;
    font-weight: 700;

    color: #3e7cb1;
}
</style>