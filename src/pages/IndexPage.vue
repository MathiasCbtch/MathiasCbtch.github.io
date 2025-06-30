<template>
  <q-page class="row items-center justify-center">
    <q-card class="shared-container">
      <ExampleComponent
        title="Hello World"
        subtitle="Cavatech Tutorial"
        subsubtitle="tutorial"
        active
      />
      <ButtonComponent buttontext="Click here" link="https://www.combitech.se/" />
    </q-card>
  </q-page>
</template>

<script setup lang="ts">
import ExampleComponent from 'components/ExampleComponent.vue';
import ButtonComponent from 'components/ButtonComponent.vue';
</script>

<style scoped lang="scss">
.shared-container {
  background-color: #ffffff;
  padding: 24px;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
  max-width: 500px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 16px;
  font-family: 'Segoe UI', sans-serif;
}
</style>
