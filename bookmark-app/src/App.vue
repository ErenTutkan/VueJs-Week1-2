<template lang="">
   <app-header></app-header>
    <div class="container">
      <app-bookmark />
    </div>
</template>
<script>
import appBookmark from '@/components/appBookmark'
import appHeader from '@/components/appHeader'
export default {
  components:{
    appBookmark,
    appHeader

  }
}
</script>
<style lang="">
  
</style>