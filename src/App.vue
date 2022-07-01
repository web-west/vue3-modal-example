<template>
  <ModalComponent id="1" header="Header-1" content="Content-1" />
  <ModalComponent id="2" header="Header-2" content="Content-2" />
  <ModalComponent id="3" header="Header-3" content="Content-3" />
  <!-- <ModalComponent header="Header-2" content="Content-2" /> -->
</template>

<script>
import ModalComponent from "./components/ModalComponent.vue";

export default {
  name: "App",
  components: {
    ModalComponent,
  },
};
</script>

<style>
</style>
