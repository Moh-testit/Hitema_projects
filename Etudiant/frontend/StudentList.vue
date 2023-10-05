<template>
    <div>
      <h2>Liste des étudiants</h2>
      <ul>
        <li v-for="student in students" :key="student.id">
          {{ student.name }}
          <span v-if="isStudentPresent(student.name)" class="present-marker"> (Présent)</span>
          <span v-else-if="isStudentAbsent(student.name)" class="absent-marker"> (Absent)</span>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      students: Array,
      presentStudents: Array,
      absentStudents: Array,
    },
    methods: {
      isStudentPresent(studentName) {
        return this.presentStudents.some(student => student.name === studentName);
      },
      isStudentAbsent(studentName) {
        return this.absentStudents.some(student => student.name === studentName);
      },
    },
  };
  </script>
  
  <style>
  .present-marker {
    color: green;
  }
  
  .absent-marker {
    color: red;
  }
  </style>
  