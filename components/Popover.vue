<template>
  <img
    src="../assets/img/question.svg"
    alt="question"
    data-bs-toggle="popover"
    data-bs-placement="right"
    data-bs-content="Default tooltip. Here you’ll find something on the left."
  />
</template>

<script>
import { onMounted } from "vue";
export default {
  setup() {
    onMounted(() => {
      const popoverTriggerList = document.querySelectorAll(
        '[data-bs-toggle="popover"]'
      );
      [...popoverTriggerList].forEach((popoverTriggerEl) => {
        new window.bootstrap.Popover(popoverTriggerEl, {
          trigger: "hover",
        });
      });
    });
  },
};
</script>

<style lang="scss">
.popover {
  width: 191px;
  height: 100px;
  background-color: rgba(30, 41, 57, 1);
  border-radius: 4px;
  border: 1px solid rgba(30, 41, 57, 1);
}

.popover-arrow::after {
    border-right-color: #1e2939 !important;
}

.popover-body {
  line-height: 22.4px;
  text-align: center;
  color: #ffffff;
  padding: 16px;
}
</style>
