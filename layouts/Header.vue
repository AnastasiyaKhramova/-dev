<template>
    <header class="container header">
        <div class="second-container find">
            <div class="find-wrapper">
                <img class="find-img" src="../assets/img/lupa.png" alt="lupa" />
                <input class='find-input' type="text" placeholder='Search for courses, lessons, resources an...'
                    v-model="searchTerm" aria-label="Find product" @input="debouncedHandleSearchChange" />
            </div>
            <nav class="nav">
                <a href="#">All Courses</a>
                <a href="#">For Business</a>
                <hr>
                <a href="#">Log In</a>
                <button class="nav__btn">Get Started</button>
            </nav>
        </div>
    </header>
</template>

<script lang="ts" setup>
import { useDebounceFn } from '@vueuse/core';
const searchTerm = ref('');
const skip = ref(0);
const handleSearchChange = (value: String) => {
    const search = value.toLowerCase();
    searchTerm.value = search;
    skip.value = 0;
};

const debouncedHandleSearchChange = useDebounceFn((e) => {
    handleSearchChange(e.target.value);
}, 1000);
</script>

<style lang="scss" scoped>
.header {
    height: 636px;
    background-image: url('../assets/img/background.png');
    background-repeat: no-repeat;
    z-index: 2;
}

.find {
    display: flex;
    justify-content: space-between;
}

.find-wrapper {
    position: relative;
    display: flex;
    align-items: center;
}

.find-img {
    position: absolute;
    left: 17px;
    width: 16px;
    height: 16px;
}

.find-input {
    width: 391px;
    height: 40px;
    padding: 10.5px 16px 10.5px 48px;
    background-color: transparent;
    border: 1px solid $blockcolor;
    border-radius: 50px;
    color: $blockcolor;
}

.find-input::placeholder {
    color: $blockcolor;
}

.nav {
    width: 476px;
    display: flex;
    align-items: center;
    gap: 32px;

    &__btn {
        width: 124px;
        height: 40px;
        border: 1px solid $blockcolor;
        border-radius: 4px;
        font-weight: 700;
        line-height: 28.8px;
        text-align: center;
        background-color: transparent;
        color: $blockcolor;
    }
}

hr {
    height: 40px;
    border-left: 1px solid rgba(221, 222, 224, 1);
}
</style>