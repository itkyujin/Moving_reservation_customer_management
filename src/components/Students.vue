<template>
 <v-flex sm8 offset-sm2>
    {{students}}
    <v-card>
      <v-toolbar dark>
        <v-toolbar-title>Students</v-toolbar-title>
      </v-toolbar>
      <v-list>
        <v-list-tile v-for="(student, index) in students" :to="'editStudent/' + index">
          <v-list-tile-content>
            <v-list-tile-title v-text="student.name"></v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-card>
  </v-flex>
</template>

<script>
import axios from "axios";
import store from "../store.js";

export default {
    data() {
        return {
            students: store.state.students
        }
    },
  async created() {
  }
};
</script>