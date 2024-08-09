<template>
    <div>
      <h2>Liste des employés</h2>
      <ol>
        <li v-for="employee in employees" :key="employee.id" @mouseover="hover=true" @mouseleave="hover=false"
        :class="{ hover: hover }">
          {{ employee.name }}
        </li>
      </ol>
    </div>
  </template>
  
  <script>
  export default {
    name: 'EmployeeList',
    data() {
      return {
        hover: false,
        employees: [
          { id: 1, name: 'Alice Dupont' },
          { id: 2, name: 'Bernard Martin' },
          { id: 3, name: 'Catherine Leroy' },
          { id: 4, name: 'David Durand' },
          { id: 5, name: 'Émilie Dubois' }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  ol {
    list-style-type: decimal;
    padding-left: 20px;
  }
  
  li {
    padding: 10px;
    font-size: 16px;
    color: #333;
    transition: color 0.3s, background-color 0.3s;
  }
  
  li.hover {
    color: white;
    background-color: #007bff;
  }
  </style>
  