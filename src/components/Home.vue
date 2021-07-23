<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">

      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Home',

  data() {
    return {
      list: [
        {
          text: 'Do something',
          color: '',
          isDone: false,
          date: '',
        },
        {
          text: 'Do something new',
          color: '',
          isDone: false,
          date: '',
        },
      ],
    };
  },
};
</script>
