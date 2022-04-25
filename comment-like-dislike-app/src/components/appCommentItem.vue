<template>
   <div class="card mb-10 comment--item">
        <p>
         {{item.text}}
        </p>
        <div class="action--button--container text-right mt-10">
          <button class="btn-sm btn-success" @click="comment.like++">Beğendim ({{item.like}})</button>
          <button class="btn-sm btn-danger" @click="comment.dislike++">Beğenmedim ({{item.dislike}})</button>
        </div>
      </div>
</template>
<script>
export default {
    props:['item'],
    data(){
        return {
            comment:this.item
        }
    }
}
</script>
<style lang="">
    
</style>