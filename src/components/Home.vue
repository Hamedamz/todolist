<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <to-do-form @add="addItem"/>
      </v-col>
    </v-row>

    <v-row>
      <v-col v-for="(item, i) in list" :key="i" cols="12">
        <to-do-card
          :todo="item"
          @set-color="color => setColor(i, color)"
        />
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

  methods: {
    addItem(text) {
      this.list.unshift({
        text,
        color: 'white',
        isDone: false,
        date: new Date().toISOString().slice(0, 22),
      });
    },

    setColor(i, color) {
      this.list[i].color = color;
    },
  },
};
</script>
