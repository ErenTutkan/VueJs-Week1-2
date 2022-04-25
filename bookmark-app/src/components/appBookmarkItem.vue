<template lang="">
  <div class="bookmark-item">
    <div class="header">
      <input
        type="text"
        class="mt-10 mb-10"
        v-model="bookmark.title"
        v-if="edit"
      />
      <h3 v-else>{{ item.title }}</h3>
      <button
        class="btn-sm btn-danger"
        @click="$emit('delete-item', item.id)"
        v-if="!edit"
      >
        Kaydı Sil
      </button>
    </div>
    <textarea
      class="mt-10 mb-10"
      name=""
      id=""
      v-model="bookmark.description"
      v-if="edit"
      rows="2"
    ></textarea>
    <p class="mt-20 mb-20" v-else>{{ item.description }}</p>
    <div>
      <input type="text" v-model="bookmark.link" class="mt-5" v-if="edit" />
      <button
        class="btn-primary btn-sm mr-5"
        v-else
        @click="gotoPage(item.link)"
      >
        Göster
      </button>
      <button class="btn-sm btn-info" @click="edit = true" v-if="!edit">
        Düzenle
      </button>
      <button class="btn-sm btn-success ml-20" @click="edit = false" v-else>
        Kaydet
      </button>
    </div>
  </div>
</template>
<script>
export default {
  props: ["item"],
  data() {
    return {
      edit: false,
      bookmark: this.item,
    };
  },
  methods: {
    gotoPage(link) {
      location.href = link;
    },
  },
};
</script>
<style lang=""></style>
