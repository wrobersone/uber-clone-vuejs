<template>
  <div class="flex items-center" id="AutoCompleteInput">
    <input :id="theId" v-model="inputComputed" @click="emit('isActive', true)" type="text" :placeholder="placeholder" class="text-md w-full py-2.5 px-3 appearance-none bg-gray-100 text-gray-700 leading-tight focus:outline-none focus:shadow-outline focus:bg-gray-200" autocomplete="off">
    <WindowCloseIcon @click="emit('isActive', true)" fillColor="#2E2E2E" />
  </div>
</template>

<script setup>
import { toRefs, defineProps, defineEmits, computed } from 'vue'
import WindowCloseIcon from "vue-material-design-icons/WindowClose.vue"

const emit = defineEmits(['update:input', 'clearInput', 'isActive'])

const props = defineProps({
  theId: String,
  input: String,
  placeholder: String,
})
const { theId, input, placeholder } = toRefs(props)
const inputComputed = computed({
  get: () => input.value,
  set: (val) => emit('update:input', val),
})
</script>
