<template>
    <div class="men">
        <div class="left">
            <img src="../assets/left-img.png" alt="">
        </div>
        <div class="text">
            <div class="about">
                <div class="antony">
                    <h2 class="name">ANTONY*</h2>
                    <p class="desc">68-year-old male newly <br>diagnosed with mCSPC</p>
                    <button class="btn">READ STORY</button>
                    <p class="star">*Not an actual patient</p>
                </div>
                <div class="tom">
                    <h2 class="name">TOM*</h2>
                    <p class="desc">76-year-old male with <br>mCSPC and a comorbidity</p>
                    <button class="btn">READ STORY</button>
                    <p class="star">*Not an actual patient</p>
                </div>
            </div>
            <div class="mSCPC">mCSPC = metastatic castration-sensitive prostate cancer</div>
        </div>
        <div class="right">
            <img src="../assets/right-img.png" alt="">
        </div>
    </div>
</template>

<script>
export default {
    name: "Card"
}
</script>

<style scoped>
.men {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

.left {
    width: 30%;

    display: flex;
    align-items: flex-end;
}

.left img {
    width: 100%;
    margin-bottom: 195px;
}

.text {
    width: 40%;
    display: flex;
    flex-direction: column;
}

.about {
    display: flex;
    justify-content: space-between;
    margin-top: 15%;
}

.antony {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.tom {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.name {
    font-size: 40px;
    font-weight: 700;
    line-height: 1.5;
}

.desc {
    margin-bottom: 16px;

    font-size: 19px;
    text-align: center;
}

.btn {
    margin-bottom: 12px;
    padding: 10px 21px;

    font-weight: 600;
    font-size: 15px;

    color: #fff;
    background-color: #3e7cb1;
    border-style: none;
}

.star {
    color: #575757;
}

.mSCPC {
    margin-top: 45px;
    text-align: center;

}

.right {
    width: 30%;
    display: flex;
    align-items: flex-end;

}

.right img {
    width: 100%;
    margin-bottom: 195px;
}
</style>