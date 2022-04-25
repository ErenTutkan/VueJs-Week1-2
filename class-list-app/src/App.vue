<template>
 <div>
<app-header></app-header>
<div class="container">
  <app-text />
</div>
 </div>
</template>

<script>
import appText from '@/components/appText'
import appHeader from '@/components/appHeader'
export default {
  components:{
    appHeader,
    appText
  }
  
}
</script>

<style>

</style>
