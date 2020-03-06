<template>
  <div class="home">
    <v-container>
      <v-row class="d-flex flex-row align-center">
        <v-col cols="10">
          <v-text-field name="name" label="Task" id="id"></v-text-field>
        </v-col>
        <v-col cols="2">
          <v-btn block color="success">Add</v-btn>
        </v-col>
      </v-row>

      <v-card>
        <v-card-title primary-title>
          <v-container>
            <v-row
              class="d-flex flex-row align-center"
              v-for="(item, index) in todos"
              :key="index"
            >
              <v-col cols="12" class="d-flex flex-row align-center">
                <v-checkbox v-model="value" value="value" />
                <span>{{ item.title }}</span>
                <v-spacer></v-spacer>
                <v-btn color="error">x</v-btn>
              </v-col>
              <v-col cols="12">
                <v-divider> </v-divider>
              </v-col>
            </v-row>
          </v-container>
        </v-card-title>
      </v-card>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "home",
  components: {},
  data() {
    return {
      todos: [
        { id: 1, title: "React", completed: false },
        { id: 2, title: "Angular", completed: true },
        { id: 3, title: "Vue", completed: false }
      ]
    };
  }
};
</script>
