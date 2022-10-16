<script lang="ts" setup>
interface ProgressBarProps {
  done: number;
  reverse?: boolean;
}

const props = defineProps<ProgressBarProps>();
</script>

<template>
  <div>
    <div class="progress" :class="{ 'progress--revert': props.reverse }">
      <div class="progress__done" :style="{ width: props.done + '%' }">
        <div class="progress-text">{{ props.done }}%</div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.progress {
  width: 500px;
  height: 50px;
  display: flex;
  background: #ccc;
  border-radius: 6px;

  &--revert {
    justify-content: flex-end;
  }

  &__done {
    height: 100%;
    width: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    background: dodgerblue;
    transition: all 0.3s ease-in-out;
    border-radius: 6px;
  }
}
</style>
