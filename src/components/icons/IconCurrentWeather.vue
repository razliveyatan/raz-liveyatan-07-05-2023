<script setup lang="ts">
import { defineProps } from 'vue';

defineProps<{
  iconUrl: string|null
}>();
</script>

<template>
    <div class="icon-current-weather show">
      <img v-if="iconUrl !== '' && iconUrl" :src="iconUrl" alt="Icon" class="weather-icon" />
      <svg v-else class="placeholder-icon" viewBox="0 0 288 288" width="88" height="88">
        <g stroke-width="9.36" fill="none" fill-rule="evenodd">
          <path d="M137.342 141.12c-16.031-34.95-12.064-75.817 10.39-107.031-54.063 8.173-94.085 54.555-94.256 109.231.02 4.899.348 9.791.983 14.648M68.733 199.48a111.478 111.478 0 0 0 190.663 2.012c-38.06 8.573-77.794-3.933-104.083-32.76" stroke="#686763" stroke-linejoin="bevel"></path>
          <path d="M124.893 138.64h-4.071a37.44 37.44 0 0 0-66.55 22.464h-5.99c-10.242.506-18.287 8.957-18.287 19.211 0 10.255 8.045 18.706 18.287 19.212h76.611a30.467 30.467 0 1 0 0-60.84v-.047Z" stroke="#BABABA"></path>
        </g>
      </svg>
    </div>
  </template>

<style scoped>
.icon-current-weather {
  display: flex;
  align-items: center;
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.3s ease, transform 0.3s ease;
}

.icon-current-weather.show {
  opacity: 1;
  transform: translateY(0);
}

.icon-current-weather img {
  width: 75px;
  height: 45px;
}

.icon-current-weather svg {
  width: 75px;
  height: 45px;
}
</style>