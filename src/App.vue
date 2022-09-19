<template>
  <div>
    <h3>Vue 3 change image size with input slider example</h3>
    <div class="np-slide-container">
      {{ sliderValue }}%
      <input
        type="range"
        min="1"
        max="100"
        v-model="sliderValue"
        class="np-slider"
      />
    </div>

    <div class="np-img-container">
      <img
        src="https://picsum.photos/id/46/600/400"
        :style="{
          width: `${sliderValue}%`,
          borderRadius: '10px',
        }"
      />
    </div>
    <!--
      www.nightprogrammer.com
    -->
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      sliderValue: 35,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.np-slide-container {
  width: 300px;
  margin: 0 auto;
}

.np-img-container {
  max-width: 600px;
  margin: 0 auto;
}

.np-slider {
  -webkit-appearance: none;
  width: 100%;
  height: 20px;
  background: #131313;
  border-radius: 20px;
  outline: none;
  opacity: 0.7;
  -webkit-transition: 0.2s;
  transition: opacity 0.2s;
  margin: 10px 0;
}

.np-slider:hover {
  opacity: 1;
}

.np-slider::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 35px;
  height: 20px;
  background: #acacac;
  border-radius: 20px;
  cursor: pointer;
}

.np-slider::-moz-range-thumb {
  width: 35px;
  height: 20px;
  background: #acacac;
  border-radius: 20px;
  cursor: pointer;
}
</style>
