<script setup>
import { ref } from 'vue'

let id = 1


const newTodo = ref('')
const todos = ref([
    { id: id++, text: 'belajar html'},
    { id: id++, text: 'belajar css'},
    { id: id++, text: 'belajar javascript'},
])

function addTodo(){
    todos.value.push({id: id++,text: newTodo.value
    })
    newTodo.value = ''

}

function removeTodo(todo){
    todos.value = todos.value.filter((t) => t.id !== todo.id)
}

</script>

<template>
    <form @submit.prevent="addTodo">
        <input v-model="newTodo" required placeholder="Tambahkan data">
        <button type="submit">Add Todo</button>
    </form>
    <ul>
        <li v-for="todo in todos" :key="todo.id">
            {{todo.id}} {{ todo.text }}
            <button @click="removeTodo(todo)">Hapus</button>
        </li>
    </ul>
</template>