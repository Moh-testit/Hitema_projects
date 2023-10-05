<template>
    <div>
      <h2>Marquer la présence/absence</h2>
      <button @click="markPresence('Joseph')">Présent Joseph</button>
      <button @click="markAbsence('Joseph')">Absent Joseph</button>
      <button @click="markPresence('Nassera')">Présent Nassera</button>
      <button @click="markAbsence('Nassera')">Absent Nassera</button>
      <button @click="markPresence('James')">Présent James</button>
      <button @click="markAbsence('James')">Absent James</button>
      <button @click="markPresence('Mohamed')">Présent Mohamed</button>
      <button @click="markAbsence('Mohamed')">Absent Mohamed</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      markPresence(studentName) {
        this.$emit('mark-presence', studentName);
      },
      markAbsence(studentName) {
        this.$emit('mark-absence', studentName);
      },
    },
  };
  </script>
  