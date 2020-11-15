<template>
    <div class="container">
        <hr>
        <div class="form-todo form group">
            <p>
                <input type="text" placeholder="Author" v-model="comment.author"
                class="form-control">
            </p>
            <p>
                <textarea v-model="comment.message" placeholder="Comment" class="form-control"></textarea>
            </p>
            <button type="submit" class="btn btn-primary"
                    @click="submit()">Add</button>
        </div>
         
    </div>
    
</template>

<script>
import bus from '../bus'
export default {
    data : () => ({
        comment: {
            author : '',
            message : ''
        }
    }),
    methods:{
        submit(){
            bus.$emit('submit', this.comment);
            
        }
    }
}
</script>

<style lang="stylus" scoped>

</style>