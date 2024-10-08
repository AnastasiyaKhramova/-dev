<template>
    <table>
        <tr>
            <td></td>
            <td>
                <div>
                    <p>All-Access Membership</p>
                    <h3>Basic</h3>
                    <p>$564 / year</p>
                </div>
            </td>
            <td>
                <div>
                    <p>All-Access Membership</p>
                    <h3>Full-Immersion</h3>
                    <p>$924 / year</p>
                </div>
            </td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>All 100+ Courses</h2>
                    <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"
                        :src="question" alt="question">
                </div>
            </td>
            <td><img :src="yesBasic" alt="yesBasic"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>All Certificate Programs</h2>
                    <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"
                        :src="question" alt="question">
                </div>
            </td>
            <td><img :src="yesBasic" alt="yesBasic"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>Quizzes, Assignments, and Tests</h2>
                </div>
            </td>
            <td><img :src="yesBasic" alt="yesBasic"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>Excel, PPT, and PDF Files</h2>
                </div>
            </td>
            <td><img :src="yesBasic" alt="yesBasic"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>Digital Blockchain Verified Certificate</h2>
                </div>
            </td>
            <td><img :src="yesBasic" alt="yesBasic"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>Another Shared Benefit</h2>
                </div>
            </td>
            <td><img :src="yesBasic" alt="yesBasic"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>Another Shared Benefit</h2>
                </div>
            </td>
            <td><img :src="no" alt="no"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>Exclusive Partner Integrations</h2>
                    <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"
                        :src="question" alt="question">
                </div>
            </td>
            <td><img :src="no" alt="no"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>Premium Email Support</h2>
                    <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"
                        :src="question" alt="question">
                </div>
            </td>
            <td><img :src="no" alt="no"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>Model Review & Feedback</h2>
                    <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"
                        :src="question" alt="question">
                </div>
            </td>
            <td><img :src="no" alt="no"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>Model Review & Feedback</h2>
                    <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"
                        :src="question" alt="question">
                </div>
            </td>
            <td><img :src="no" alt="no"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>Résumé & Cover Letter Review</h2>
                    <img v-b-popover.hover.right="'Default tooltip. Here you’ll find something on the left.'"
                        :src="question" alt="question">
                </div>
            </td>
            <td><img :src="no" alt="no"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td>
                <div>
                    <h2>One FREE Financial Modeling Competition Entry</h2>
                </div>
            </td>
            <td><img :src="no" alt="no"></td>
            <td><img :src="yesFull" alt="yesFull"></td>
        </tr>
        <tr>
            <td></td>
            <td>
                <div>
                    <h3>Basic</h3>
                    <p>$564 / year</p>
                    <Button />
                </div>
            </td>
            <td>
                <div>
                    <h3>Full-Immersion</h3>
                    <p>$924 / year</p>
                    <Button />
                </div>
            </td>
        </tr>
    </table>
</template>

<script>
import question from '../assets/img/question.svg'
import yesBasic from '../assets/img/yesBasic.png'
import yesFull from '../assets/img/yesFull.png'
import no from '../assets/img/no.png'
import Button from './Button.vue';
</script>

<style lang="scss" scoped></style>