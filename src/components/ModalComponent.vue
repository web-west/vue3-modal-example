<template>
  <button class="modal-open" @click="isOpen = true">Open Modal {{id}}</button>
  <teleport to="body">
    <transition name="opacity">
      <div class="modal" v-if="isOpen">
        <div class="modal-wrapper">
          <div class="modal-header">{{ header }}</div>
          <div class="modal-content">{{ content }}</div>
          <div class="modal-buttons">
            <button @click="isOpen = false">Close</button>
          </div>
        </div>
      </div>
    </transition>
  </teleport>
</template>

<script>
import { ref } from "vue";
export default {
  props: {
    id: {
      type: [Number,String],
      default: "",
    },
    header: {
      type: String,
      default: "",
    },
    content: {
      type: String,
      default: "",
    },
  },
  setup(props) {
    const isOpen = ref(false);
    return { isOpen, props };
  },
};
</script>