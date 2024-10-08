<template>
    <section class="card">
        <div class="card__heading">
            <h3>Most benefits!</h3>
        </div>
        <div class="card__conteiner">
            <div>
                <h3>All Access Membership</h3>
                <h2>Full-Immersion</h2>
            </div>
            <div>
                <p>Everything in the Basic plan, plus more</p>
            </div>
            <div>
                <h2>$77/month <span>(pay annually — $924 / year)</span></h2>
            </div>
            <Button />
            <div></div>
            <div>
                <p>Everything in Basic, plus:</p>
            </div>
            <div>
                <ul>
                    <li>Capital IQ & EIKON Partner Integrations</li>
                    <li>Premium Email Support <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"  src="../assets/img/question.svg" alt="question"></li>
                    <li>Model Review & Feedback <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"  src="../assets/img/question.svg" alt="question"></li>
                    <li>Additional Case Studies <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"  src="../assets/img/question.svg" alt="question"></li>
                    <li>Resume & Cover Letter Review</li>
                    <li>A FREE Modeling Competition Entry</li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
import Button from './Button'
export default {
    data() {
        return {
            selected: ''
        }
    }
}
</script>

<style lang="scss" scoped>
.card {
    width: 544px;
}

.card__heading {
    background: $basiccolor;
}
</style>