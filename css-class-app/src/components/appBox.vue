<template>
<div class="container css--class--app">
      <div class="card text-center">
        <ul class="css--palette text-center">
          <li v-for="item in color" :key="item.id" :style="item" @click="changeColor(item.id)"></li>
          
        </ul>
        <div class="result-box" :style="selectColor" ></div>
      </div>
    </div>
</template>
<script>
export default{
    data(){
        return {
            color:[
                {
                    id:1,
                    'background-color':'red'
                }
                ,{
                    id:2,
                    'background-color':'green'
                },
                {
                    id:3,
                    'background-color':'blue'
                }
            ],
            selectColor:null
        }
    },
    methods:{
        changeColor(colorId){
            this.selectColor=this.color.filter(c=>c.id===colorId);
            console.log(this.selectColor)
        }
    }
}
</script>
<style>
</style>