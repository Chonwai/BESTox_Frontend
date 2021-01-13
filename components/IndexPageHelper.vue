<template>
  <div class="index-page-helper-component">
    <v-alert icon="mdi-alert-circle-outline" prominent dense text type="info">
      <v-row align="center">
        <v-col class="grow"> You have uploaded the job already? </v-col>
        <v-col class="shrink">
          <v-btn @click="showRetrieve = true">Click here to retrieve</v-btn>
          <TaskRetrieveDialog
            :dialog="showRetrieve"
            v-on:dialogToggle="retrieveDialogCallback"
          />
        </v-col>
      </v-row>
    </v-alert>
    <v-alert
      border="left"
      colored-border
      color="deep-purple accent-4"
      elevation="2"
    >
      BESTox is a convolutional neural network regression model for acute oral
      toxicity prediction. The model was trained and evaluated on the Oral Rat
      LD50 data set. In a benchmark dataset, this model achieved 0.619, 0.603,
      0.433 for R2 (squared Pearson correlation coefficient), RMSE and MAE
      respectively.
    </v-alert>
  </div>
</template>

<script>
import TaskRetrieveDialog from './TaskRetrieveDialog'
export default {
  name: 'IndexPageHelper',
  components: {
    TaskRetrieveDialog,
  },
  data() {
    return {
      showRetrieve: false,
    }
  },
  methods: {
    retrieveDialogCallback(toggle) {
      this.showRetrieve = toggle
    },
  },
}
</script>
