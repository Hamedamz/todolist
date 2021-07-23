<template>
<v-card>
  <v-sheet
    height="4"
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

    <v-menu offset-y left>
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          icon
          v-bind="attrs"
          v-on="on"
        >
          <v-icon>mdi-palette</v-icon>
        </v-btn>
      </template>

      <v-sheet color="white">
        <v-btn
          icon
          @click="setColor('white')"
        >
          <v-icon>mdi-water-off</v-icon>
        </v-btn>

        <v-btn
          v-for="color in colors"
          :key="color"
          :color="color"
          icon
          @click="setColor(color)"
        >
          <v-icon>mdi-circle</v-icon>
        </v-btn>
      </v-sheet>
    </v-menu>
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
