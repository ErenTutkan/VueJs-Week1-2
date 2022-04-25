<template lang="">
    <div>
         <div class="comment--like--dislike--app">
            <appCommentItem v-for="comment in comments" :key="comment.id" :item="comment"/>
         </div>
    </div>
</template>
<script>
import appCommentItem from '@/components/appCommentItem'
export default {
    data(){
        return {
            comments:[
                {
                    id:1,
                    text:`Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sint deserunt, tempore
                         accusamus iusto nobis dolore ratione itaque perferendis delectus? Nostrum
                         corporis, quod voluptates quis consequuntur eveniet beatae dolor aperiam ad.
                         `,
                         like:0,
                         dislike:5
                },
                { id:2, text:`Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sint
deserunt, tempore accusamus iusto nobis dolore ratione itaque perferendis
delectus? Nostrum corporis, quod voluptates quis consequuntur eveniet beatae
dolor aperiam ad. `, like:5, dislike:5 },

{ id:3, text:`Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sint
deserunt, tempore accusamus iusto nobis dolore ratione itaque perferendis
delectus? Nostrum corporis, quod voluptates quis consequuntur eveniet beatae
dolor aperiam ad. `, like:7, dislike:3 }
,
{ id:4, text:`Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sint
deserunt, tempore accusamus iusto nobis dolore ratione itaque perferendis
delectus? Nostrum corporis, quod voluptates quis consequuntur eveniet beatae
dolor aperiam ad. `, like:2, dislike:1 }

            ]
        }
    },
    components:{
        appCommentItem
    }
    
}
</script>
<style lang="">
    
</style>