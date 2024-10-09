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

<style lang="scss" scoped>
.popover {
  width: 191px;
  background-color: rgba(30, 41, 57, 1);
  border: 1px solid rgba(30, 41, 57, 1);
}

.popover-arrow {
  border-top-color: #1e2939;
}

.popover-body {
  font-size: 14px;
  font-weight: 400;
  line-height: 22.4px;
  text-align: center;
  color: #ffffff;
}
</style>
