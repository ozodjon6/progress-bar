<template>
  <div class="progress-bar">
    <div :class="(progress === 100) ? 'progress-bar__inner complete' : 'progress-bar__inner' "
         :style="`width: ${progress}%`">
      <span :class="progress > 50 ? 'white' : ''">{{progress}}%</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProgressBar",
  props: ['progress']
}
</script>

<style scoped>
  .progress-bar {
    position: relative;
  }

  .progress-bar__inner {
    width: 100%;
    height: 20px;
    background-image: linear-gradient(to right, #ED008D, #2484E4);
    border-radius: 0 10px 10px 0;
  }

  .progress-bar__inner span {
    position: absolute;
    text-align: center;
    color: #182E45;
    right: 50%;
  }
  .progress-bar__inner.complete {
    border-radius: 0;
  }

  .progress-bar__inner .white {
    color: #ffffff;
  }
</style>