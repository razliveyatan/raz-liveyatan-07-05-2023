<script setup lang="ts">
defineProps<{
  cityName: string|null,
  temperature:number,
  tempertauteType:string,
}>();
</script>
<template>
    <div class="destination-details-container" :class="{ 'show': cityName !== ''}">
        <p class="city-name">{{cityName}}</p>
        <p class="temperature">{{temperature}}°{{ tempertauteType }}</p>
    </div>
</template>

<style scoped>
.destination-details-container {
  margin-left: 10px;    
  transition: opacity 0.3s ease, transform 0.3s ease;
}
.temperature , .city-name{
  font-size: 18px;
  font-weight: bold;
  margin-right: 5px;
}

/* .destination-details-container.show {
  opacity: 1;
  transform: translateY(0);
} */
</style>