<template>
  <div>
    <Header />
    <Main />
    <Table/>
    <Faq/>
    <Feedback/>

  </div>
</template>

<script lang="ts" setup>
import Header from '~/layouts/Header.vue';
import Main from '~/components/Main.vue';
import Table from '~/components/Table.vue'
import Faq from '~/components/Faq.vue';
import Feedback from '~/components/Feedback.vue';
</script>