<template lang="">
  <div>
    <div class="bookmark--app--container">
      <appBookmarkItem
        v-for="bookmark in bookmarks"
        :key="bookmark.id"
        :item="bookmark"
        @delete-item="deleteItem($event)"
      />
    </div>
  </div>
</template>
<script>
import appBookmarkItem from "./appBookmarkItem.vue";
export default {
  components: {
    appBookmarkItem,
  },
  data() {
    return {
      bookmarks: [
        {
          id: 1,
          title: "Bookmark 1",
          description: "Açıklama 1",
          link: "https://www.google.com",
        },
        {
          id: 2,
          title: "Bookmark 2",
          description: "Açıklama 2",
          link: "https://www.google.com",
        },

        {
          id: 3,
          title: "Bookmark 3",
          description: "Açıklama 3",
          link: "https://www.google.com",
        },

        {
          id: 4,
          title: "Bookmark 4",
          description: "Açıklama 4",
          link: "https://www.google.com",
        },
      ],
    };
  },
  methods: {
    deleteItem(item) {
      this.bookmarks = this.bookmarks.filter((c) => c.id !== item);
    },
  },
};
</script>
<style lang=""></style>
