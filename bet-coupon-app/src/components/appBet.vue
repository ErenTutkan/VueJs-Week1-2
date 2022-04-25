<template lang="">
  <div
    class="bet--coupon--app d-flex justify-content-between align-items-start"
  >
    <match-list :matchesList="matches" />
    <app-coupon :coupon="coupon" :rate="couponrate"></app-coupon>
  </div>
</template>
<script>
import matchList from "./matchList.vue";
import appCoupon from "./appCoupon.vue";
export default {
  components: {
    matchList,
    appCoupon,
  },
  provide() {
    return {
      addCouponMatch: this.addCouponMatches,
      deleteCouponMatch: this.deleteCouponMatches
    };
  },
  data() {
    return {
      matches: [
        {
          id: 1,
          matchName: "Fenerbahçe x Galatasaray",
          home: 1.5,
          draw: 2.5,
          away: 2.3,
          hour: "19:00",
        },
        {
          id: 2,
          matchName: "Fenerbahçe x Beşiktaş",
          home: 1.3,
          draw: 2.9,
          away: 2.1,
          hour: "20:00",
        },
        {
          id: 3,
          matchName: "Fenerbahçe x Başakşehir",
          home: 1.2,
          draw: 3.1,
          away: 2.2,
          hour: "21:00",
        },
      ],
      coupon: [],
      couponrate: 1

    };
  },
  methods: {
    addCouponMatches(item) {

      if (this.coupon.filter(c => c.id === item.id).length > 0) {
        this.deleteCouponMatches(item)
      }

      this.coupon.push(item);
      this.couponrate *= item.rate;


    },
    deleteCouponMatches(item) {

      this.coupon = this.coupon.filter(c => c.id !== item.id)
      this.couponrate /= item.rate
    },

  },
};
</script>
<style lang=""></style>
