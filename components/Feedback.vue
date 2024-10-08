<template>
    <section class="container slider-container">
        <h1>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis</h1>
        <div>
            <button class="controls" @click="prevSlide" :disabled="currentPage === 0"><img
                    src="@/assets/img/prevSlide.png" alt="prevSlide"></button>
            <div class="slider">
                <div class="slide" v-for="slide in slides" :key="slide.id">
                    <img class="slide__img" :src="slide.photo" alt="Photo">
                    <h3 class="slide__title">{{ slide.name }} <span>{{ slide.profession }}</span></h3>
                    <p class="slide__desc">{{ slide.description }}</p>
                    <a class="slide__more" href="#">{{ slide.more }}</a>
                </div>
            </div>
            <button class="controls" @click="nextSlide" :disabled="currentPage === maxPage"><img
                    src="@/assets/img/nextSlide.png" alt="nextSlide"></button>
        </div>
    </section>
</template>

<script>
import { uuidv4 } from 'uuidv4';

export default {
    data() {
        return {
            slides: [
                {
                    id: uuidv4(),
                    photo: require('@/assets/img/photo.png'),
                    name: 'John Doe',
                    profession: 'Financial Controller',
                    description: '“Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis ut vehicula sapien. Nam a tortor nulla. Sed sed erat eget enim feugiat dapibus et non justo ...”',
                    more: 'Read more'
                },
                {
                    id: uuidv4(),
                    photo: require('@/assets/img/photo.png'),
                    name: 'John Doe',
                    profession: 'Financial Controller',
                    description: '“Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis ut vehicula sapien. Nam a tortor nulla. Sed sed erat eget enim feugiat dapibus et non justo ...”',
                    more: 'Read more'
                },
                {
                    id: uuidv4(),
                    photo: require('@/assets/img/photo.png'),
                    name: 'John Doe',
                    profession: 'Financial Controller',
                    description: '“Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis ut vehicula sapien. Nam a tortor nulla. Sed sed erat eget enim feugiat dapibus et non justo ...”',
                    more: 'Read more'
                },
                {
                    id: uuidv4(),
                    photo: require('@/assets/img/photo.png'),
                    name: 'John Doe',
                    profession: 'Financial Controller',
                    description: '“Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis ut vehicula sapien. Nam a tortor nulla. Sed sed erat eget enim feugiat dapibus et non justo ...”',
                    more: 'Read more'
                },
                {
                    id: uuidv4(),
                    photo: require('@/assets/img/photo.png'),
                    name: 'John Doe',
                    profession: 'Financial Controller',
                    description: '“Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis ut vehicula sapien. Nam a tortor nulla. Sed sed erat eget enim feugiat dapibus et non justo ...”',
                    more: 'Read more'
                }, {
                    id: uuidv4(),
                    photo: require('@/assets/img/photo.png'),
                    name: 'John Doe',
                    profession: 'Financial Controller',
                    description: '“Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis ut vehicula sapien. Nam a tortor nulla. Sed sed erat eget enim feugiat dapibus et non justo ...”',
                    more: 'Read more'
                }
            ],
            itemsPerPage: 3,
            currentPage: 0,
        }
    },
    computed: {
        pageCount() {
            return Math.ceil(this.sections.length / this.itemsPerPage);
        },
        visibleSections() {
            const start = this.currentPage * this.itemsPerPage;
            return this.sections.slice(start, start + this.itemsPerPage);
        },
        maxPage() {
            return this.pageCount - 1;
        }
    },
    methods: {
        prevSlide() {
            this.currentPage--;
        },
        nextSlide() {
            this.currentPage++;
        },
        goToPage(page) {
            this.currentPage = page;
        }
    }
}
</script>

<style lang="scss" scoped>
.slider-container {
    height: 250px;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    background-color: white;
    border-radius: 20px;
    position: relative;
    top: -30px;
    z-index: 1;
}

.slider {
    display: flex;
    cursor: pointer;
}

.slide {
    width: 350px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;

    &__img {
        width: 47px;
    }

    &__title {
        font-size: 18px;
        font-weight: 600;
        color: rgba(30, 41, 57, 1);
        line-height: 4.51px;
        text-align: center;
    }

    &__title span {
        font-size: 16px;
        font-weight: 400;
        color: rgba(28, 125, 135, 1);
    }

    &__desc {
        font-size: 16px;
        font-weight: 400;
        line-height: 24.84px;
        text-align: left;
        color: $textcolor;
    }

    &__more {
        font-size: 16px;
        font-weight: 700;
        line-height: 24.84px;
        text-align: left;
        color: $fullcolor;
    }
}

.controls {
    width: 64px;
    height: 64px;
    cursor: pointer;
}
</style>