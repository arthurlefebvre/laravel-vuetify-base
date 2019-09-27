<template>
  <div>
    <v-btn color="pink" rounded class="white--text">Hello World !</v-btn>
    <v-btn bottom color="pink" dark fab fixed right @click="dialog = !dialog">
      <v-icon>mdi-plus</v-icon>
    </v-btn>
    <v-dialog v-model="dialog" width="800px">
      <v-card>
        <v-card-title class="blue darken-3 white--text">Create contact</v-card-title>
        <v-container>
          <v-row>
            <v-col cols="12">
              <v-text-field prepend-icon="mdi-account-circle" placeholder="Name"></v-text-field>
            </v-col>
            <v-col cols="6">
              <v-text-field prepend-icon="business" placeholder="Company"></v-text-field>
            </v-col>
            <v-col cols="6">
              <v-text-field placeholder="Job title"></v-text-field>
            </v-col>
            <v-col cols="12">
              <v-text-field prepend-icon="mail" placeholder="Email"></v-text-field>
            </v-col>
            <v-col cols="12">
              <v-text-field type="tel" prepend-icon="phone" placeholder="(000) 000 - 0000"></v-text-field>
            </v-col>
            <v-col cols="12">
              <v-text-field prepend-icon="notes" placeholder="Notes"></v-text-field>
            </v-col>
          </v-row>
        </v-container>
        <v-card-actions>
          <v-btn text color="primary">More</v-btn>
          <div class="flex-grow-1"></div>
          <v-btn outlined color="error" @click="dialog = false">Cancel</v-btn>
          <v-btn outlined color="primary" @click="dialog = false">Save</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  data: () => ({
    dialog: false
  })
};
</script>