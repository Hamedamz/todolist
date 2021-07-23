<template>
<v-card flat>
  <v-form>
    <v-card-title>
      <v-text-field
        v-model="text"
        filled
        rounded
        hide-details
        placeholder="What to do?"
      />

      <v-btn
        depressed
        rounded
        large
        type="submit"
        color="grey darken-4"
        class="ml-4 white--text"
        :disabled="!text"
      >
        add
      </v-btn>
    </v-card-title>
  </v-form>
</v-card>
</template>

<script>
export default {
  name: 'ToDoForm',

  data() {
    return {
      text: '',
    };
  },
};
</script>
