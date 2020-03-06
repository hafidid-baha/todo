<template>
    <div class="">
        <h4>Add New Todo</h4>
        <form @submit.prevent="addTodoSubmit">
            <div class="form-group">
                <input type="text" v-model="todoTitle" class="form-control" placeholder="Todo Title">
                <input type="submit" value="Add Post" class="btn btn-primary mt-2 mb-2" />
            </div>
        </form>
    </div>
</template>
<script>
import { mapActions } from 'vuex';
export default {
    name:'AddTodo',
    data(){
        return{
            todoTitle: ''
        }
    },
    methods:{
        ...mapActions(['addTodo']),
        addTodoSubmit(){
            this.addTodo(this.todoTitle)
        }
    }
}
</script>