<template>
  <div id="app">
    <StudentList :students="students" :presentStudents="presentStudents" :absentStudents="absentStudents" />
    <AttendanceButtons @mark-presence="markPresence" @mark-absence="markAbsence" />
    <AttendanceStatus :presentStudents="presentStudents" :absentStudents="absentStudents" />
  </div>
</template>

<script>
import StudentList from "frontend/StudentList.vue";
import AttendanceButtons from "frontend/AttendanceStatus.vue";
import AttendanceStatus from "frontend/AttendanceStatus.vue";

export default {
  data() {
    return {
      students: [
        { id: 1, name: "Joseph" },
        { id: 2, name: "Nassera" },
        { id: 3, name: "James" },
        { id: 4, name: "Mohamed" },
      ],
      presentStudents: [],
      absentStudents: [],
    };
  },
  components: {
    StudentList,
    AttendanceButtons,
    AttendanceStatus,
  },
  methods: {
    markPresence(studentName) {
      const studentIndex = this.students.findIndex(student => student.name === studentName);
      if (studentIndex !== -1) {
        this.presentStudents.push(this.students[studentIndex]);
        const absentIndex = this.absentStudents.findIndex(student => student.name === studentName);
        if (absentIndex !== -1) {
          this.absentStudents.splice(absentIndex, 1);
        }
      }
    },
    markAbsence(studentName) {
      const studentIndex = this.students.findIndex(student => student.name === studentName);
      if (studentIndex !== -1) {
        this.absentStudents.push(this.students[studentIndex]);
        const presentIndex = this.presentStudents.findIndex(student => student.name === studentName);
        if (presentIndex !== -1) {
          this.presentStudents.splice(presentIndex, 1);
        }
      }
    },
  },
};
</script>

<style>
@import "/Users/mohamedmazuicloud.com/Documents/Hitema_projects/Etudiant/frontend/src/styles.css";
</style>
