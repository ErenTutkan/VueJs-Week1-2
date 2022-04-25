<template>
  <div>
    <app-header />
    <!-- App Comment-->
    <div class="container">
        <app-comment />

    </div>
    
  </div>
</template>

<script>
import appHeader from '@/components/appHeader'
import appComment from '@/components/appComment'
export default{
  components:{
    appComment,
    appHeader
  }
}
</script>


<style>

</style>
