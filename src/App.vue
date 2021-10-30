<template>
  <div>
    <button style="" @click="showModal = true">Show Modal</button>
    <teleport to="#modal-root">
      <Modal v-show="showModal" @close="showModal = false">
        <Basic />
      </Modal>
    </teleport>
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";
import Basic from "./components/BasicTemplate.vue";
export default {
  name: "App",
  components: {
    Modal,
    Basic,
  },
  data() {
    return {
      showModal: false,
    };
  },
};
</script>
