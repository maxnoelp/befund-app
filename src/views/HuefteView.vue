<template>
  <div class="container">
    <div class="mt-4">
      <h1 class="text-decoration-underline text-center">Befundstest Hüfte</h1>
    </div>
    <div class="middle-content d-flex justify-content-center align-items-center pb-5">
      <BefundHuefteView />
    </div>
  </div>
</template>
<script>
import BefundHuefteView from '@/components/BefundHuefteView.vue';

export default {
  components: { BefundHuefteView },
};
</script>
<style>
.container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.middle-content {
  flex-grow: 1;
}
</style>
