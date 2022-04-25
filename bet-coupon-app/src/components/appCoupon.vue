<template>
  <div class="coupon--total--container">
    <div class="card my-coupon">
      <div class="card--header">
        <h4>Kuponum</h4>
      </div>
      <div class="card--body">
        <app-coupon-item v-for="item in coupon" :key="item.id" :item="item"></app-coupon-item>

      </div>
    </div>
    <app-coupon-result :cuoponrate="rate"></app-coupon-result>
  </div>
</template>
<script>
import appCouponItem from "./appCouponItem.vue";
import appCouponResult from "./appCouponResult";
export default {
  components: {
    appCouponItem,
    appCouponResult,
  },
  props: {
    coupon: {
      type: Array,
      required: true
    },
    rate: Number,
  }
};
</script>
<style lang=""></style>
