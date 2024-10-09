<template>
    <section class="container">
        <h1 class="feedback__title">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros
            aliquam mattis</h1>
        <div class="slider-container">
            <button class="controls" @click="prevSlide" :disabled="currentPage === 0">
                <img src="@/assets/img/prevSlide.png" alt="prevSlide">
            </button>
            <div class="slider">
                <div class="slide" v-for="slide in visibleSections" :key="slide.id">
                    <div class="slide__headding">
                        <img class="slide__img" :src="slide.photo" alt="Photo">
                        <h3 class="slide__title">{{ slide.name }} <h4>{{ slide.profession }}</h4></h3>
                    </div>
                    <p class="slide__desc">{{ slide.description }}</p>
                    <a class="slide__more" href="#">{{ slide.more }}</a>
                </div>
            </div>
            <button class="controls" @click="nextSlide" :disabled="currentPage === maxPage">
                <img src="@/assets/img/nextSlide.png" alt="nextSlide">
            </button>
        </div>
    </section>
</template>

<script>
import { v4 as uuidv4 } from 'uuid';
import photo from '../assets/img/photo.png'

export default {
    data() {
        return {
            slides: [
                {
                    id: uuidv4(),
                    photo: photo,
                    name: 'John Doe',
                    profession: 'Financial Controller',
                    description: '“Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis ut vehicula sapien. Nam a tortor nulla. Sed sed erat eget enim feugiat dapibus et non justo ...”',
                    more: 'Read more'
                },
                {
                    id: uuidv4(),
                    photo: photo,
                    name: 'John Doe',
                    profession: 'Financial Controller',
                    description: '“Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis ut vehicula sapien. Nam a tortor nulla. Sed sed erat eget enim feugiat dapibus et non justo ...”',
                    more: 'Read more'
                },
                {
                    id: uuidv4(),
                    photo: photo,
                    name: 'John Doe',
                    profession: 'Financial Controller',
                    description: '“Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis ut vehicula sapien. Nam a tortor nulla. Sed sed erat eget enim feugiat dapibus et non justo ...”',
                    more: 'Read more'
                },
                {
                    id: uuidv4(),
                    photo: photo,
                    name: 'John Doe',
                    profession: 'Financial Controller',
                    description: '“Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis ut vehicula sapien. Nam a tortor nulla. Sed sed erat eget enim feugiat dapibus et non justo ...”',
                    more: 'Read more'
                },
                {
                    id: uuidv4(),
                    photo: photo,
                    name: 'John Doe',
                    profession: 'Financial Controller',
                    description: '“Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur at erat eget eros aliquam mattis ut vehicula sapien. Nam a tortor nulla. Sed sed erat eget enim feugiat dapibus et non justo ...”',
                    more: 'Read more'
                }, {
                    id: uuidv4(),
                    photo: photo,
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
            return Math.ceil(this.slides.length / this.itemsPerPage);
        },
        visibleSections() {
            const start = this.currentPage * this.itemsPerPage;
            return this.slides.slice(start, start + this.itemsPerPage);
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
.feedback__title {
    width: 920px;
    padding-top: 80px;
    font-size: 32px;
    font-weight: 700;
    line-height: 44px;
    text-align: center;
    color: $fullcolor;
    margin: 0 auto;
}

.slider-container {
    margin-top: 108px;
    height: 250px;
    display: flex;
    align-items: center;
    padding: 0 29px;
    justify-content: space-between;
}

.slider {
    display: flex;
    gap: 34px;
}

.slide {
    background-color: $blockcolor;
    width: 350px;
    height: 327px;
    display: flex;
    flex-direction: column;
    padding: 32px;

    &__headding {
        width: 286px;
        display: flex;
        gap: 25px;
        margin-bottom: 22px;
    }

    &__img {
        height: 47px;
    }

    &__title {
        font-size: 18px;
        font-weight: 600;
        color: rgba(30, 41, 57, 1);
    }

    &__title h4 {
        font-size: 16px;
        font-weight: 400;
        color: rgba(28, 125, 135, 1);
    }

    &__desc {
        line-height: 24.84px;
        color: $textcolor;
        margin-bottom: 16px;
    }

    &__more {
        font-weight: 700;
        color: $fullcolor;
    }
}

.controls {
    width: 64px;
    height: 64px;
    background-color: $basiccolor;
    border: 1px solid $basiccolor;
    border-radius: 50px;
    cursor: pointer;
}
</style>