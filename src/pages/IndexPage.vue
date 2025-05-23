<template>
  <q-page class="row items-center justify-evenly">
    <ExampleComponent
      title="Hello World 12345"
      subtitle="Cavatech Tutorial"
      tutorial="tutorial"
      str="söp"
      active
    />
    <ButtonComponent buttontext="Click here" />
  </q-page>
</template>

<script setup lang="ts">
import ExampleComponent from 'components/ExampleComponent.vue'
import ButtonComponent from 'components/ButtonComponent.vue'
</script>
