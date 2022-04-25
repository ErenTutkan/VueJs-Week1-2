<template lang="">
<li class="course-item list-item" :class="[{'bg-success ':item.isDone},{'bg-danger':!item.isDone}]">
            <span>{{item.title}}</span>
            <input type="checkbox" v-model="itemLocal.isDone" />
 </li>
</template>
<script>
export default {
    props:['item'],
   data(){
       return{
            itemLocal:this.item
       }
      
   },
}
</script>
<style lang="">
    
</style>