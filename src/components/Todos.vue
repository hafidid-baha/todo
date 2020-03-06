<template>
    <div class="todos">
        <h2>All The Todos</h2>
        <div class="row">
            <div class="col-4 mt-2 mb-2 position-relative" v-for="todo in allTodos" :key="todo.id">
                <div class="todo rounded pt-4 pb-4">{{todo.title}}</div>
                <div class="position-absolute text-white close" @click="deleteTodo(todo.id)">x</div>
            </div>
        </div>
    </div>
</template>
<script>
// import the maGetters To Get Data From The State
import {mapGetters,mapActions} from 'vuex';
export default {
    name:'Todos',
    computed: mapGetters(['allTodos']),
    methods:{
        ...mapActions(['fetchTodos','deleteTodo'])
    },
    created(){
        this.fetchTodos()
    }
}
</script>
<style scoped>
    .close{
        width: 30px;
        height: 30px;
        border:1px solid white;
        border-radius: 50%;
        right:30px;
        bottom: 5px;
        line-height: 25px;
        text-align: center;
        cursor: pointer;
    }
</style>