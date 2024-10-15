<template>
  <section class="card">
    <h3 class="card__heading">Most benefits!</h3>
    <div class="card__conteiner">
      <div>
        <h4 class="card__conteiner_title">All Access Membership</h4>
        <h3 class="card__conteiner_type">Full-Immersion</h3>
      </div>
      <div>
        <p class="card__conteiner_desc">
          Everything in the Basic plan, plus more
        </p>
      </div>
      <div class="card__cost">
        <div class="card__cost_choice">
          <h2 class="card__cost_price">$77<span> /month </span></h2>
          <p>(pay annually — $924 / year)</p>
        </div>
      </div>
      <Button button-color="rgba(19, 46, 87, 1)" />
      <div>
        <p class="card__include">Everything in Basic, plus:</p>
      </div>
      <div>
        <ul class="card__include_items">
          <li>Capital IQ & EIKON Partner Integrations</li>
          <li>
            Premium Email Support
            <Popover />
          </li>
          <li>
            Model Review & Feedback
            <Popover />
          </li>
          <li>
            Additional Case Studies
            <Popover />
          </li>
          <li>Resume & Cover Letter Review</li>
          <li>A FREE Modeling Competition Entry</li>
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
.card {
  width: 544px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  border-radius: 10px;
  color: $fullcolor;
  border: none;
  position: absolute;
  right: 121px;
  bottom: -95px;

  &__heading {
    min-height: 32px;
    font-size: 14px;
    font-weight: 700;
    line-height: 22.4px;
    justify-content: center;
    align-items: center;
    display: flex;
    background: $fullcolor;
    color: $blockcolor;
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;
  }

  &__conteiner {
    padding: 48px;
    display: flex;
    flex-direction: column;
    gap: 24px;

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
      gap: 15px;
      list-style-image: url(../assets/img/check-full.png);
      padding-left: 24px;
    }

    &_items li {
      padding-left: 6px;
    }
  }
}
</style>
