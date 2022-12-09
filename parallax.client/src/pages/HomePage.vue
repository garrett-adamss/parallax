<template>
  <div class="test"></div>
  <div class="test">
    <div class="rellax" data-rellax-speed="-3">
    slowish
    </div>
    <div class="rellax" data-rellax-speed="7">
      fast rellax testing
    </div>
    <div class="rellax" data-rellax-speed="-5">
      slow
    </div>
  </div>
</template>

<script>

export default {
  setup() {

    return {

    }
  },
}
</script>

<style scoped lang="scss">
.test{
  height: 200vh;
}
</style>
