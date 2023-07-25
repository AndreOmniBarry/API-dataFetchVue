<template>
    <div>
      <h1>Population Data</h1>
      <button class="button" @click="fetchData">Fetch Data</button>
      <ul>
        <li v-for="item in data" :key="item.ID">
          {{ item.Geography }}: {{ item.Population }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        data: []
      };
    },
    mounted() {
      this.fetchData();
    },
    methods: {
      async fetchData() {
        try {
          const response = await fetch('https://datausa.io/api/data?drilldowns=Nation&measures=Population');
          const jsonData = await response.json();
          this.data = jsonData.data;
        } catch (error) {
          console.error('Error fetching data:', error);
        }
      }
    }
  };
  </script>
  