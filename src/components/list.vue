<template>
    <div class="list-group">
        <div v-for="comment in comments" :key="comment.message" class="list-group-item">
            <p>{{comment.message}}</p>
            <span class="comment_author">
             <strong>{{comment.author}}</strong>
            </span>
        </div>
    </div>    
</template>

<script>
import bus from '../bus'

export default {
    data : () => ({
        comments : [{
            author : '',
            message : ''
        }]
    }),
     mounted (){
         bus.$on('submit',(comment) => this.comments.unshift(comment) );
     }
    
}
</script>

<style lang="stylus" scoped>

</style>