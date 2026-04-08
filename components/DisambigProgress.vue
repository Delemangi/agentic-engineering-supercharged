<!--
  DisambigProgress — Segmented progress bar for disambiguation slides.

  Usage:
    <DisambigProgress :step="1" />   (1-based, out of 9 steps)

  Shows labeled dots along a track. Current step is accent-lit, past steps are dimmed, future steps are dark.
-->
<script setup lang="ts">
defineProps<{
  step: number
}>()

const steps = [
  'Model',
  'Tokens',
  'LLM vs Agent',
  'Harness',
  'Enhancements',
  'Tools',
  'Skills',
  'MCPs',
  'Context Window',
]
</script>

<template>
  <div class="dp-wrap">
    <div class="dp-track">
      <div class="dp-fill" :style="{ width: ((step - 1) / (steps.length - 1)) * 100 + '%' }" />
    </div>
    <div class="dp-labels">
      <div
        v-for="(label, i) in steps"
        :key="i"
        class="dp-step"
        :class="{
          'dp-done': i + 1 < step,
          'dp-active': i + 1 === step,
          'dp-future': i + 1 > step,
        }"
      >
        <div class="dp-dot" />
        <span class="dp-label">{{ label }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.dp-wrap {
  position: fixed;
  bottom: 1rem;
  left: 3rem;
  right: 3rem;
  z-index: 50;
  width: auto;
  padding: 0 0 0.25rem 0;
}

.dp-track {
  position: absolute;
  top: 5px;
  left: 0;
  right: 0;
  margin: 0 calc(100% / 18);
  height: 3px;
  background: rgba(255, 255, 255, 0.08);
  border-radius: 3px;
  z-index: 0;
}

.dp-fill {
  height: 100%;
  border-radius: 3px;
  background: var(--nc-accent, #E30613);
  box-shadow: 0 0 8px rgba(var(--nc-accent-rgb, 227, 6, 19), 0.5);
  transition: width 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.dp-labels {
  display: flex;
  justify-content: space-between;
  position: relative;
  z-index: 1;
}

.dp-step {
  display: flex;
  flex-direction: column;
  align-items: center;
  flex: 1;
}

.dp-dot {
  width: 11px;
  height: 11px;
  border-radius: 50%;
  border: 2px solid rgba(255, 255, 255, 0.15);
  background: var(--nc-bg, #0c0c0c);
  transition: all 0.3s ease;
}

.dp-active .dp-dot {
  background: var(--nc-accent, #E30613);
  border-color: var(--nc-accent, #E30613);
  box-shadow: 0 0 10px rgba(var(--nc-accent-rgb, 227, 6, 19), 0.6);
}

.dp-done .dp-dot {
  background: rgba(var(--nc-accent-rgb, 227, 6, 19), 0.4);
  border-color: rgba(var(--nc-accent-rgb, 227, 6, 19), 0.5);
}

.dp-label {
  font-size: 0.45rem;
  margin-top: 4px;
  color: rgba(255, 255, 255, 0.2);
  text-align: center;
  white-space: nowrap;
  transition: color 0.3s ease;
}

.dp-active .dp-label {
  color: var(--nc-accent, #E30613);
  font-weight: 700;
}

.dp-done .dp-label {
  color: rgba(255, 255, 255, 0.35);
}
</style>
