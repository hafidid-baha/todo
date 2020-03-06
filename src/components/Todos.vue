<template>
    <div class="todos">
        <h2>All The Todos</h2>
        <div class="row">
            <div class="col-4 mt-2 mb-2" v-for="todo in allTodos" :key="todo.id">
                <div class="todo rounded pt-4 pb-4">{{todo.title}}</div>
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
        ...mapActions(['fetchTodos'])
    },
    created(){
        this.fetchTodos()
    }
}
</script>