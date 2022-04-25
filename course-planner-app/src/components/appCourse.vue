<template lang="">
       <div class="course--planner-app--container">
           <appNewCourse :addNewItem="addNewItem"></appNewCourse>
            <appCourseList :courses="course"></appCourseList>
      <div class="mt-10">
        <small>Toplam {{getTotalCount}} adet kursunuz var.</small> <br>
        <small>İzlenmiş {{getDoneCount}} adet kursunuz var.</small><br>
        <small>İzlenmemiş {{getNotDoneCount}} adet kursunuz var.</small>
      </div>
    </div>
</template>
<script>
import appNewCourse from '@/components/appNewCourse'
import appCourseList from './appCourseList'
export default {
    components:{
        appNewCourse,
        appCourseList
    },
    data(){
        return {
            course:[
                {
                    id:1,
                    title:'Vuejs',
                    isDone:true
                },
                {
                    id:2,
                    title:'ReactJs',
                    isDone:false
                },
                {
                    id:3,
                    title:'AngularJs',
                    isDone:false
                },
            ]
        }
    },
    methods:{
        addNewItem(item){
            console.log()
            this.course.push({
                id:new Date().getTime(),
                title:item,
                isDone:false
            })
        }
    },
    computed:{
        getDoneCount(){
            return this.course.filter(c=>c.isDone===true).length
        },
        getNotDoneCount(){
            return this.course.filter(c=>c.isDone===false).length
        },
        getTotalCount(){
            return this.course.length
        }
    }
}
</script>
<style lang="">
    
</style>