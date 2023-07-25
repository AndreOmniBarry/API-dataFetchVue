<template>
  <div>
    <PopulationData />
  </div>
</template>

<script>
import PopulationData from './components/PopulationData.vue';

export default {
  components: {
    PopulationData
  }
};
</script>

<style>
.button {
  background-color: #3c3b6e;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  font-size: 16px;
  cursor: pointer;
}

.button:hover {
  background-color: #c8102e;
}
</style>
