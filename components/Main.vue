<template>
    <main class="container">
        <div class="second-container main">
            <h1 class="main__headding">Pricing Plans</h1>
            <h4 class="main__subheadding">Upgrade your skills. Choose a plan that works for your budget and career
                goals.</h4>
                <div class="cards">
                    <BasicCard />
                    <FullCard />
                </div>
            </div>
    </main>
</template>

<script>
import BasicCard from './BasicCard.vue';
import FullCard from './FullCard.vue';
export default {

}
</script>

<style lang="scss" scoped>
.main {
    position: absolute;
    top: 144px;
    left: 190px;

    &__headding {
        font-size: 56px;
        font-weight: 700;
        line-height: 72px;
        text-align: center;
        color: $blockcolor;
    }

    &__subheadding {
        font-size: 18px;
        font-weight: 400;
        line-height: 28.8px;
        text-align: center;
        color: $blockcolor;
        margin-top: 32px;
        margin-bottom: 156px;
    }
}

.cards {
    display: flex;
    justify-content: space-between;
}
</style>