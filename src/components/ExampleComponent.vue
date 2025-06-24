<template>
  <div class="example-wrapper">
    <p class="title-text">{{ title }}</p>
    <p class="sub-title-text">{{ subtitle }}</p>
    <p class="tutorial">{{ tutorial }}</p>
  </div>
</template>

<script setup lang="ts">
interface Props {
  title: string;
  subtitle: string;
  tutorial: string;
}

defineProps<Props>();
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
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.title-text {
  color: $primary;
  font-size: 28px;
  font-weight: bold;
  margin-bottom: 16px;
}

.sub-title-text {
  color: $secondary;
  font-size: 21px;
  font-weight: bold;
  margin-bottom: 16px;
}

.tutorial {
  color: $accent;
  font-size: 16px;
  margin-bottom: 16px;
}

.testing {
  background-color: #ffffff;
  padding: 24px;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
  max-width: 500px;
  width: 100%;
  font-family: 'Segoe UI', sans-serif;
  margin: 0 auto;
}
</style>
