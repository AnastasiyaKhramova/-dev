<template>
    <section class="card">
        <div class="card__heading">
            <h3>Most popular!</h3>
        </div>
        <div class="card__conteiner">
            <div>
                <h3>All Access Membership</h3>
                <h2>Basic</h2>
            </div>
            <div>
                <p>Includes all courses from many programs</p>
            </div>
            <div>
                <h2>Pick your plan:</h2>
                <div>
                    <b-form-group label="Individual radios" v-slot="{ ariaDescribedby }">
                        <b-form-radio v-model="selected" :aria-describedby="ariaDescribedby" name="some-radios" value="A" checked>$47/month <span>(pay annually — $564 / year)</span> <div>Save 30%!</div>
                        </b-form-radio>
                        <b-form-radio v-model="selected" :aria-describedby="ariaDescribedby" name="some-radios"  value="B">$87/month <span>(pay per month)</span></b-form-radio>
                    </b-form-group>
                </div>
            </div>
            <Button />
            <div></div>
            <div>
                <p>Includes:</p>
            </div>
            <div>
                <ul>
                    <li>All 100+ Courses <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"  src="../assets/img/question.svg" alt="question"></li>
                    <li>All 4 Certificate Programs <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"  src="../assets/img/question.svg" alt="question"></li>
                    <li>Excel, PPT, and PDF Files</li>
                    <li>Digital Blockchain Verified Certificates</li>
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