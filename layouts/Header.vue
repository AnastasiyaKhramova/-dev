<template>
    <header class="container">
        <div class="second-container header">
            <input class='catalog__find' type="text" placeholder='Search for courses, lessons, resources an...'
                aria-label="Find product" @change={  debouncedHandleSearchChange } />
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

<script setup>
const handleSearchChange = (e) => {
    const search = e.target.value.toLowerCase();
    setSearchTerm(search);
    setSkip(0);
};

const debouncedHandleSearchChange = useCallback(debounce(handleSearchChange, 1000), []);
</script>

<style lang="scss" scoped>
.header {
    min-width: $container;
    background: image('../assets/img/background.png');
}

.nav {
    width: 476px;
    height: 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 32px;
    font-size: 16px;
    line-height: 19px;
    font-weight: 400;

    &__btn {
        width: 124px;
        border: 1px solid $blockcolor;
        border-radius: 4px;
        font-weight: 700;
        line-height: 28.8px;
        text-align: center;
    }
}

hr {
    width: 1px;
}

.lang {
    display: flex;
    gap: 16px;
}

.start {
    font-size: 20px;
    line-height: 20px;
    color: #ffffff;
    background-color: $primary-color;
    border-radius: 25px;
    width: 145px;
    height: 52px;
}
</style>