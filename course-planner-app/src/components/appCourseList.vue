<template lang="">
    <div class="card card-light mt-20">
        <h3>Aktif Kurslarım</h3>
        <ul class="list mt-20">
          <course-item v-for="course in courses" :key="course.id" :item="course"/>
        </ul>
      </div>
</template>
<script>
import courseItem from './courseItem'
export default {
    components:{
        courseItem
    },
    props:['courses']
    
}
</script>
<style lang="">
    
</style>