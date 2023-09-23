<script setup>

import {onMounted, onUpdated, ref} from 'vue';
import Modal from "./Modal.vue";


const props = defineProps(['steps']);
const stepsLength = props.steps.length;
const index = ref(0);
const showModal = ref(true);

onMounted(() => {
  positionModal();
});

onUpdated(() => {
  if (!showModal.value) return;
  positionModal();
});

let modalElement = null;

function positionModal() {
  modalElement = document.querySelector('.modal-container');
  modalElement.classList.remove("animation");
  modalElement.style.opacity = 0;
  const targetElementBoundingRect = document.querySelector(props.steps[index.value].target).getBoundingClientRect();
  modalElement.style.top = `${targetElementBoundingRect.top + targetElementBoundingRect.height}px`;

  const targetElementMiddlePositionX = targetElementBoundingRect.left + (targetElementBoundingRect.width / 2);
  modalElement.style.left = `${targetElementMiddlePositionX - (modalElement.getBoundingClientRect().width / 2)}px`;

  modalElement.classList.add("animation");
  modalElement.style.opacity = 100;
}

function handleNext() {
  ++index.value;
}

function handleBack() {
  --index.value;
}

</script>

<template>
  <Teleport to="body">
<!--    <Modal class="modal" :show="showModal" @close="showModal = false" :target="props.steps[index].target">-->
    <Modal class="modal" :show="showModal" @close="showModal = false" :target="props.steps[index].target">

<!--      <template #header>-->
<!--        <h3>custom header</h3>-->
<!--      </template>-->
      <template #body>
        <div class="content">{{props.steps[index].content}}</div>
      </template>

      <template #footer>
        <div class="action-buttons">
          <button class="skip action" @click="showModal=false">
            {{ (index + 1) < stepsLength ? 'Skip' : 'Ok'}}
          </button>

          <div class="navigation-buttons">
            <div @click="handleBack" :class="{'hidden': index === 0}" class="action">Back</div>
            <div @click="handleNext" :class="{'hidden': (index + 1) === stepsLength}" class="action">Next</div>
          </div>
        </div>
      </template>


    </Modal>
  </Teleport>

</template>


<style scoped>

.content {
  font-weight: bold;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}

.action-buttons {
  display: flex;
  justify-content: space-between;
  gap: 2rem;
  align-items: center;
}

.navigation-buttons {
  display: flex;
  gap: 1rem;
}

.hidden {
  visibility: hidden;
}

.action:hover {
  cursor: pointer;
}

@keyframes fade-in {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

</style>

