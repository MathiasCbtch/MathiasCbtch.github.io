<template>
    <div class="example-button">
        <button class="button-primary">
            {{ buttontext }}
        </button>
    </div>

</template>

<script setup lang="ts">
interface Props {
  buttontext: string
}

defineProps<Props>()
</script>

<style lang="scss">
@import 'src/css/quasar.variables.scss';

.example-button {
  background-color: #ffffff;
  padding: 24px;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
  max-width: 500px;
  width: 100%;
  font-family: 'Segoe UI', sans-serif;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center; 
  justify-content: center;
}

.button-primary {
  color: $primary;
  font-size: 28px;
  font-weight: bold;
  margin-bottom: 16px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
}

</style>
