<script setup>

const props = defineProps(['show']);

</script>

<template>
    <div v-if="show" class="modal-mask">
      <div :class="{ 'hidden': false }"  class="modal-container animation">
        <div class="mod al-header">
          <slot name="header"></slot>
        </div>

        <div class="mod al-body">
          <slot name="body">default body</slot>
        </div>

        <div class="mo dal-footer">
          <slot name="footer">
            default footer
            <button
                class="modal-default-button"
                @click="$emit('close')"
            >Skip</button>
          </slot>
        </div>
      </div>
    </div>
</template>

<style>
.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  transition: opacity 0.3s ease;
}


.animation {
  animation: fade-in 0.5s ease-in;
}

.modal-container {
  max-width: 250px;
  margin: auto;
  padding: 20px 30px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);

  position: absolute;
  color: gray;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

@keyframes fade-in {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

@media (min-width: 768px) {
  .modal-container {
    max-width: 400px;
  }
}

.modal-default-button {
  float: right;
}

.hidden {
  visibility: hidden;
}

</style>
