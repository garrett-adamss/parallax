<template>
  <div class="root">
    <img class="background" ref="background" src="https://images.unsplash.com/photo-1537420327992-d6e192287183?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=988&q=80" />
    <img
      class="foreground"
      ref="foreground"
      src="https://914230.smushcdn.com/2260515/wp-content/uploads/2021/06/RS-Header-Moon_840px_3.png?lossy=1&strip=1&webp=1"
    />
    <div class="section section-1" ref="first">
      <div>
        <h1>Parallax Made Easy.</h1>
      </div>
    </div>
    <div class="section section-2" ref="second">
      <div>
        <h2>Here's more info</h2>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit...</p>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, onMounted, onUnmounted } from 'vue'
export default {
  setup() {
    const foreground = ref(null)
    const background = ref(null)
    const first = ref(null)
    const second = ref(null)
    return {
      foreground,
      background,
      first,
      second,
    }
  },
}
</script>

<style scoped lang="scss">
img.background,
img.foreground {
  /* Fill background */
  min-height: 100%;
  min-width: 1024px;
  /* Scale proportionately */
  width: 100%;
  height: auto;
}
img.background {
  /* Positioning */
  position: fixed;
  transform: rotate(-0.25turn);
  top: 0;
  left: 0;
}
.section {
  min-height: 100vh;
  position: relative;
}
.section > div {
  position: fixed;
  color: white;
  /* centers this div */
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

.section-1 {
  margin-bottom: 500px; /* determines the gap between our two sections */
  font-size: 4em;
}

.section-2 {
  opacity: 0; /* defaults to 0 because it's not visible */
}

.section-2 div {
  background-color: rgba(255, 255, 255, 0.7);
  color: black;
  text-align: center;
  padding: 50px;
  max-width: 300px;
}

.section-2 h2 {
  font-size: 2em;
  margin-bottom: 40px;
}

.section-2 p {
  line-height: 150%;
}

</style>
