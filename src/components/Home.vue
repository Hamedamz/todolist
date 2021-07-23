<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <to-do-form />
      </v-col>
    </v-row>

    <v-row>
      <v-col v-for="(item, i) in list" :key="i" cols="12">
        <to-do-card :todo="item" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import ToDoCard from './ToDoCard.vue';
import ToDoForm from './ToDoForm.vue';

export default {
  name: 'Home',

  components: {
    ToDoForm,
    ToDoCard,
  },

  data() {
    return {
      list: [
        {
          text: 'Do something',
          color: '',
          isDone: false,
          date: 'Fri, 23 Jul 2021 07:50',
        },
        {
          text: 'Do something new',
          color: '',
          isDone: false,
          date: 'Fri, 23 Jul 2021 07:50',
        },
      ],
    };
  },
};
</script>
