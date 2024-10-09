<template>
  <section class="container">
    <table class="second-container table table-bordered">
      <thead class="table-custom">
        <tr>
          <td></td>
          <td>
            <div class="table_basic-top">
              <p class="table_desc">All-Access Membership</p>
              <h4 class="table_choice">Basic</h4>
              <p class="table_cost">$564 / year</p>
            </div>
          </td>
          <td>
            <div class="table_full-top">
              <p class="table_desc">All-Access Membership</p>
              <h4 class="table_choice">Full-Immersion</h4>
              <p class="table_cost">$924 / year</p>
            </div>
          </td>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>
            <div class="table_point">
              All 100+ Courses
              <Popover />
            </div>
          </td>
          <td><img src="../assets/img/check-base.png" alt="yesBasic" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point">
              All Certificate Programs
              <Popover />
            </div>
          </td>
          <td><img src="../assets/img/check-base.png" alt="yesBasic" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point">Quizzes, Assignments, and Tests</div>
          </td>
          <td><img src="../assets/img/check-base.png" alt="yesBasic" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point">Excel, PPT, and PDF Files</div>
          </td>
          <td><img src="../assets/img/check-base.png" alt="yesBasic" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point table-block">
              Digital Blockchain Verified Certificate
            </div>
          </td>
          <td><img src="../assets/img/check-base.png" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point">Another Shared Benefit</div>
          </td>
          <td><img src="../assets/img/check-base.png" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point">Another Shared Benefit</div>
          </td>
          <td><img src="../assets/img/no.png" alt="no" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point">
              Exclusive Partner Integrations
              <Popover />
            </div>
          </td>
          <td><img src="../assets/img/no.png" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point">
              Premium Email Support
              <Popover />
            </div>
          </td>
          <td><img src="../assets/img/no.png" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point">
              Model Review & Feedback
              <Popover />
            </div>
          </td>
          <td><img src="../assets/img/no.png" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point">
              Model Review & Feedback
              <Popover />
            </div>
          </td>
          <td><img src="../assets/img/no.png" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point">
              Résumé & Cover Letter Review
              <Popover />
            </div>
          </td>
          <td><img src="../assets/img/no.png" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td>
            <div class="table_point table-block">One FREE Financial Modeling Competition Entry</div>
          </td>
          <td><img src="../assets/img/no.png" /></td>
          <td><img src="../assets/img/check-full.png" alt="yesFull" /></td>
        </tr>
        <tr>
          <td></td>
          <td>
            <div class="table_basic-bottom">
              <h3 class="table_choice">Basic</h3>
              <p class="table_cost">$564 / year</p>
              <Button style="margin-top: 12px"/>
            </div>
          </td>
          <td>
            <div class="table_full-bottom">
              <h3 class="table_choice">Full-Immersion</h3>
              <p class="table_cost">$924 / year</p>
              <Button button-color="rgba(19, 46, 87, 1)" style="margin-top: 12px"/>
            </div>
          </td>
        </tr>
      </tbody>
    </table>
  </section>
</template>

<script>
import Button from "./Button.vue";
import Popover from "./Popover.vue";
export default {};
</script>

<style lang="scss" scoped>
.table {
  text-align: center;
  table-layout: fixed;
  padding: 0;

  &_basic-top {
    border-top: 8px solid $basiccolor;
    padding: 40px 110px 32px;
  }

  &_full-top {
    border-top: 8px solid $fullcolor;
    padding: 40px 110px 32px;
  }

  &_desc {
    font-size: 14px;
    line-height: 22.4px;
    color: $lighttextcolor;
  }

  &_choice {
    font-size: 18px;
    font-weight: 700;
    line-height: 25.2px;
    color: $fullcolor;
    margin-top: 4px;
  }

  &_cost {
    line-height: 25.6px;
    color: $lighttextcolor;
  }

  &_point {
    display: flex;
    justify-content: space-between;
    padding: 0 24px;
    line-height: 25.6px;
    color: $textcolor;
    margin: auto 0;
  }

  &_basic-bottom {
    padding: 20px 101px 48px;
  }

  &_full-bottom {
    padding: 20px 101px 48px;
  }
}

.table-block {
    width: 258px;
    text-align: start;
}

tr {
    height: 80px;
    vertical-align: middle;
}
</style>
