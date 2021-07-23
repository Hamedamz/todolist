<template>
<v-card>
  <v-sheet
    height="6"
    :color="todo.color"
  />

  <v-card-title>
    <v-checkbox hide-details class="my-0 py-0"/>
    {{  todo.text }}
  </v-card-title>

  <v-card-actions>
    <v-card-subtitle class="pa-2 grey--text">
      {{ todo.date }}
    </v-card-subtitle>

    <v-spacer/>

    <v-btn icon>
      <v-icon>mdi-delete</v-icon>
    </v-btn>

    <v-btn icon>
      <v-icon>mdi-palette</v-icon>
    </v-btn>
  </v-card-actions>
</v-card>
</template>

<script>
export default {
  name: 'ToDoCard',

  props: {
    todo: {
      type: Object,
      required: true,
    },
  },
};
</script>
