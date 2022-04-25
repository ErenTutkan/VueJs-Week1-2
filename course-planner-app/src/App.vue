<template>
<div>
  <app-header />
  <div class="container">
    <app-course />


  </div>
</div>
</template>

<script>
import appCourse from '@/components/appCourse'
import appHeader from '@/components/appHeader'
export default {
components:{
  appHeader,
  appCourse
}
}
</script>

<style>

</style>
