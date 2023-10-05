<template>
    <div>
      <h2>État de présence/absence</h2>
      <ul>
        <li v-for="student in presentStudents" :key="student.id" class="present">
          {{ student.name }} - Présent
        </li>
        <li v-for="student in absentStudents" :key="student.id" class="absent">
          {{ student.name }} - Absent
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      presentStudents: Array, // Liste des étudiants présents
      absentStudents: Array, // Liste des étudiants absents
    },
  };
  </script>
  
  <style>
  .present {
    color: green;
  }
  
  .absent {
    color: red;
  }
  </style>
  