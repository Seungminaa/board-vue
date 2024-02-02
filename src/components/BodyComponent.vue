<template>
        <ul id="myUL">
            <li v-for="tod in list" v-bind:key="tod.no" @click="cancleTodo(tod.cancelFlag)">{{ tod.todo }}<span class="close"  @click="deleteTodo(tod.no)">X</span></li>
        </ul>
</template>

<script>

export default{ 
    props: ['list'],
    methods:{
        deleteTodo(no) { 
            this.$emit('todo-delete',no)
        },
        cancleTodo(cancelFlag) {
            // if(!this.cancelFlag){
                
            // }else{

            // }
            this.$emit('todo-cancle',cancelFlag)
        }
    }
}
</script>