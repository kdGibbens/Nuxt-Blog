<script setup>
const colorMode = useColorMode();

const modes = ['system', 'light', 'dark'];
const showNextModeLabel = ref(false);
const nextMode = computed(() => {
  const currentModeIndex = modes.indexOf(colorMode.preference);
  let nextModeIndex = null;
  if (currentModeIndex + 1 === modes.length) {
    nextModeIndex = 0;
  } else {
    nextModeIndex = currentModeIndex + 1;
  }

  return modes[nextModeIndex];
});
const toggleMode = () => {
  colorMode.preference = nextMode.value;
};
</script>

<template>
  <div class="flex space-x-2 items-center">
    <div class="text-gray-500 text-xs" v-if="showNextModeLabel">
      Change to {{ nextMode }}
    </div>
    <button
      @click="toggleMode"
      @mouseenter="showNextModeLabel = true"
      @mouseleave="showNextModeLabel = false"
    >
      {{ colorMode.preference.toUpperCase() }} MODE
    </button>
  </div>
</template>
