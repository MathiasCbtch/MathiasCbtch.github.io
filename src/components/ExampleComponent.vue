<template>
  <div class="example-wrapper">
    <p class="title-text">{{ title }}</p>

    <ul class="todo-list">
      <li v-for="todo in todos" :key="todo.id" @click="increment">
        {{ todo.id }} - {{ todo.content }}
      </li>
    </ul>

    <p class="meta">Count: {{ todoCount }} / {{ meta.totalCount }}</p>
    <p class="status">Active: {{ active ? 'yes' : 'no' }}</p>
    <p class="clicks">Clicks on todos: {{ clickCount }}</p>
  </div>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue'
import type { Todo, Meta } from './models'

interface Props {
  title: string
  todos?: Todo[]
  meta: Meta
  active: boolean
}

const props = withDefaults(defineProps<Props>(), {
  todos: () => []
})

const clickCount = ref(0)
function increment() {
  clickCount.value += 1
  return clickCount.value
}

const todoCount = computed(() => props.todos.length)
</script>

<style lang="scss">

@import 'src/css/quasar.variables.scss';

.example-wrapper {
  background-color: #ffffff;
  padding: 24px;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
  max-width: 500px;
  width: 100%;
  font-family: 'Segoe UI', sans-serif;
  margin: 0 auto;
}

.title-text {
  color: $primary;
  font-size: 28px;
  font-weight: bold;
  margin-bottom: 16px;
}

.todo-list {
  list-style: none;
  padding: 0;
  margin-bottom: 16px;
}

.todo-list li {
  padding: 8px 12px;
  margin-bottom: 8px;
  background-color: #f1f5f9;
  border-radius: 6px;
  cursor: pointer;
  transition: background-color 0.2s;
}

.todo-list li:hover {
  background-color: #e0ecf8;
}

.meta,
.status,
.clicks {
  margin-bottom: 8px;
  color: #555;
}
</style>
