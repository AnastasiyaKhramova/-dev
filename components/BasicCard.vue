<template>
  <section class="card">
    <h3 class="card__heading">Most popular!</h3>
    <div class="card__conteiner">
      <div>
        <h4 class="card__conteiner_title">All Access Membership</h4>
        <h3 class="card__conteiner_type">Basic</h3>
      </div>
      <div>
        <p class="card__conteiner_desc">
          Includes all courses from many programs
        </p>
      </div>
      <div class="card__cost">
        <h4 class="card__cost_title">Pick your plan:</h4>
        <div class="form-check">
          <input class="form-check-input" type="radio" name="flexRadioDefault" id="flexRadioDefault1" />
          <label class="form-check-label" for="flexRadioDefault1">
            <div class="card__cost_choice">
              <h2 class="card__cost_price">$47<span>/month </span></h2>
              <p>(pay annually — $564 / year)</p>
              <div class="card__cost_sale">Save 30%!</div>
            </div>
          </label>
        </div>
        <div class="form-check">
          <input class="form-check-input" type="radio" name="flexRadioDefault" id="flexRadioDefault2" checked />
          <label class="form-check-label" for="flexRadioDefault2">
            <div class="card__cost_choice">
              <h2 class="card__cost_price">$87<span>/month </span></h2>
              <p>(pay per month)</p>
            </div>
          </label>
        </div>
      </div>
      <Button />
      <div>
        <p class="card__include">Includes:</p>
      </div>
      <div>
        <ul class="card__include_items">
          <li>
            All 100+ Courses
            <Popover />
          </li>
          <li>
            All 4 Certificate Programs
            <Popover />
          </li>
          <li>Excel, PPT, and PDF Files</li>
          <li>Digital Blockchain Verified Certificates</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
import Button from "./Button";
import Popover from "./Popover.vue";

export default {
  data() {
    return {
      selected: "",
    };
  },
};
</script>

<style lang="scss" scoped>
.form-check {
  margin-bottom: 0;
}

.card {
  width: 544px;
  height: 731px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  border-radius: 10px;
  color: $fullcolor;
  border: none;

  &__heading {
    min-height: 32px;
    font-size: 14px;
    font-weight: 700;
    line-height: 22.4px;
    justify-content: center;
    align-items: center;
    display: flex;
    background: $basiccolor;
    color: $blockcolor;
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;
  }

  &__conteiner {
    padding: 49px;
    display: flex;
    flex-direction: column;
    gap: 22px;

    &_title {
      margin-bottom: 4px;
      font-size: 16px;
      font-weight: 400;
      line-height: 25.6px;
    }

    &_type {
      font-size: 24px;
      font-weight: 700;
      line-height: 32px;
    }

    &_desc {
      font-size: 16px;
      font-weight: 400;
      line-height: 25.6px;
      color: $textcolor;
    }
  }

  &__cost {
    display: flex;
    flex-direction: column;
    gap: 16px;

    &_title {
      font-size: 18px;
      font-weight: 700;
      line-height: 25.2px;
    }

    &_choice {
      display: flex;
      align-items: baseline;
      gap: 8px;
    }

    &_price {
      font-size: 32px;
      font-weight: 700;
      line-height: 44px;
    }

    &_price span {
      font-size: 18px;
      font-weight: 700;
      line-height: 44px;
    }

    &_choice p {
      font-size: 14px;
      font-weight: 400;
      line-height: 22.4px;
    }

    &_sale {
      width: 82px;
      height: 23px;
      background-color: rgba(233, 240, 250, 1);
      border-radius: 16px;
      color: $basiccolor;
      font-size: 14px;
      text-align: center;
    }
  }

  &__include {
    border-top: 1px solid rgba(221, 222, 224, 1);
    padding-top: 24px;
    line-height: 25.6px;
    color: $textcolor;

    &_items {
      line-height: 25.6px;
      color: $textcolor;
      display: flex;
      flex-direction: column;
      gap: 19px;
      list-style-image: url(../assets/img/check-base.png);
      padding-left: 23px;
    }

    &_items li {
      padding-left: 6px;
    }
  }
}

input[type="radio"]:checked~label {
  color: $fullcolor;
}


input[type="radio"]:not(:checked)~label {
  color: $lighttextcolor;
}
</style>
