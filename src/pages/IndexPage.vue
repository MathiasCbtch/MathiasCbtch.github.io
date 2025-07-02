<template>
  <q-page class="row items-center justify-center">
    <q-card
      class="q-pa-lg q-mx-auto q-my-xl text-center"
      style="max-width: 500px;"
    >
      <q-card-section class="column items-center q-gutter-md">
        <ExampleComponent
          title="Hello World"
          subtitle="Cavatech Tutorial"
          subsubtitle="tutorial"
          active
        />
        <ButtonComponent
          buttontext="Click here"
          link="https://www.combitech.se/"
        />
      </q-card-section>
    </q-card>
  </q-page>
</template>

<script setup lang="ts">
import ExampleComponent from 'components/ExampleComponent.vue';
import ButtonComponent from 'components/ButtonComponent.vue';
</script>
