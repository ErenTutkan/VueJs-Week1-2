<template lang="">
  <div class="competition-item">
    <div class="info--container">
      <span class="font-weight-bold">{{ item.matchName }}</span>
      <small class="text-muted mt-5"
        ><i>Saat: {{ item.hour }}</i></small
      >
    </div>
    <div class="rates">
      <div class="rate-item">
        <button class="btn-sm" @click="addMatch('1', item.home)">
          {{ item.home }}
        </button>
      </div>
      <div class="rate-item">
        <button class="btn-sm" @click="addMatch('X', item.draw)">
          {{ item.draw }}
        </button>
      </div>
      <div class="rate-item">
        <button class="btn-sm" @click="addMatch('2', item.away)">
          {{ item.away }}
        </button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    item: {
      type: Object,
      required: true,
    },
  },
  inject: ['addCouponMatch'],
  data() {
    return {
      matchItem: this.item,
    };
  },
  methods: {
    addMatch(res, resRate) {

      let match = {
        id: this.matchItem.id,
        matchName: this.matchItem.matchName,
        hour: this.matchItem.hour,
        result: res,
        rate: resRate,
      };

      this.addCouponMatch(match);
    },
  },
};
</script>
<style lang=""></style>
