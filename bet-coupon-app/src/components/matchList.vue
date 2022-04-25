<template lang="">
  <div class="card competition-list mr-10">
    <div class="card--header">
      <h4>Yakın Zamanda Başlayacak Müsabakalar</h4>
    </div>
    <div class="card--body">
      <match-item
        v-for="item in matchesList"
        :key="item.id"
        :item="item"
      ></match-item>
    </div>
  </div>
</template>
<script>
import matchItem from "./matchItem.vue";
export default {
  components: {
    matchItem,
  },
  props: {
    matchesList: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style lang=""></style>
