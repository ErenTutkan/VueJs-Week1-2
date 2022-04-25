<template lang="">
    <div class="card">
        <div class="user--action--container">
          <div class="form-group">
            <label>Kursun Adı</label>
            <input type="text" v-model="value"/>
          </div>
          <button class="btn-primary" @click="addNewItem(value)">Kurs Ekle</button>
        </div>
      </div>
</template>
<script>
export default {
    props:{
      addNewItem:{
        type:Function
        }
    },
    data(){
      return{
        value:""
      }
    }
}
</script>
<style lang="">
    
</style>