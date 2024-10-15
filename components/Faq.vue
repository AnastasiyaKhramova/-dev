<template>
    <section class="container">
        <div class="faq">
            <div>
                <h2 class="faq__title">Frequently Asked Questions</h2>
                <details class="faq__details" v-for="question in questions" :key="question.id">
                    <summary>
                        {{ question.question }}
                        <img class="faq__icon" :src="question.img" alt="plus" />
                    </summary>
                    {{ question.answer }}
                </details>
            </div>
        </div>
    </section>
</template>

<script>
import { v4 as uuidv4 } from 'uuid';
import plus from '../assets/img/plus.png'
export default {
    data() {
        return {
            questions: [
                {
                    id: uuidv4(),
                    question: 'Can I download the Excel files and financial modeling templates?',
                    answer: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa cum officia vero cupiditate provident, animi facilis? Laborum ullam mollitia modi!',
                    img: plus
                },
                {
                    id: uuidv4(),
                    question: 'How long do I have to complete the course?',
                    answer: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa cum officia vero cupiditate provident, animi facilis? Laborum ullam mollitia modi!',
                    img: plus
                },
                {
                    id: uuidv4(),
                    question: 'Are courses verified?',
                    answer: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa cum officia vero cupiditate provident, animi facilis? Laborum ullam mollitia modi!',
                    img: plus
                },
                {
                    id: uuidv4(),
                    question: 'Are there additional fees or costs? ',
                    answer: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa cum officia vero cupiditate provident, animi facilis? Laborum ullam mollitia modi!',
                    img: plus
                },
                {
                    id: uuidv4(),
                    question: 'What currency are your courses priced in?',
                    answer: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa cum officia vero cupiditate provident, animi facilis? Laborum ullam mollitia modi!',
                    img: plus
                },
                {
                    id: uuidv4(),
                    question: 'How do I earn my certificates?',
                    answer: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa cum officia vero cupiditate provident, animi facilis? Laborum ullam mollitia modi!',
                    img: plus
                },
                {
                    id: uuidv4(),
                    question: 'Can I email the instructor if I have questions?',
                    answer: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa cum officia vero cupiditate provident, animi facilis? Laborum ullam mollitia modi!',
                    img: plus
                },
                {
                    id: uuidv4(),
                    question: 'Wil these courses help me advanced my career?',
                    answer: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa cum officia vero cupiditate provident, animi facilis? Laborum ullam mollitia modi!',
                    img: plus
                },
                {
                    id: uuidv4(),
                    question: 'More questions?',
                    answer: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa cum officia vero cupiditate provident, animi facilis? Laborum ullam mollitia modi!',
                    img: plus
                }
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
.container {
    padding-top: 90px;
}

.faq {
    min-width: 880px;
    min-height: 388px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    padding: 110px 221px;
    background-color: $blockcolor;
    
    &__title {
        font-size: 32px;
        font-weight: 700;
        line-height: 44px;
        margin-bottom: 35px;
        color: $fullcolor;
        padding-right: 52px;
        text-align: center;
    }

    &__details {
        color: $fullcolor;
        font-weight: 600;
        line-height: 26px;
        border-bottom: 1px solid rgba(235, 235, 235, 1);
        padding: 14px 0;
        overflow: hidden;
        max-height: 77px;
        transition: max-height 1s ease, padding 1s ease;
    }
}


.faq__details[open] {
    max-height: 152px;
    padding: 25px 0;
    transition: max-height 1s ease, padding 1s ease;
}

.faq__details summary {
    font-size: 18px;
    font-weight: 700;
    color: rgba(103, 103, 103, 1);
    line-height: 24.51px;
    list-style: none;
    display: flex;
    justify-content: space-between;
    cursor: pointer;
}

.faq__details[open] summary {
    margin-bottom: 25px;
}

.faq__icon {
    width: 16px;
    height: 16px;
    transition: transform 1s ease;
}

.faq__details[open] .faq__icon {
    transform: rotate(45deg);
}
</style>
