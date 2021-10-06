<template>
  <v-card :loading="loading" class="mx-auto my-12" max-width="374">
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img height="100%" src="../assets/hong.png"></v-img>

    <v-card-title>홍이</v-card-title>

    <v-card-text>
      <v-row align="center" class="mx-0">
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ms-4">
          4.5
        </div>
      </v-row>

      <div class="my-4 text-subtitle-1">
        $ • Bucheon, Sangdong Lake Park
      </div>

      <div>
        10/16~10/30 누적 5.7km로 현재 선두
      </div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>

    <v-card-title>Main workout-time</v-card-title>

    <v-card-text>
      <v-chip-group
        v-model="selection"
        active-class="deep-purple accent-4 white--text"
        column
      >
        <v-chip>4:00PM</v-chip>

        <v-chip>6:00PM</v-chip>

        <v-chip>8:00PM</v-chip>

        <v-chip>10:00PM</v-chip>
      </v-chip-group>
    </v-card-text>

    <v-card-actions>
      <v-btn color="deep-purple lighten-2" text @click="reserve">
        Refresh
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    loading: false,
    selection: 3,
  }),

  methods: {
    reserve() {
      this.loading = true;

      setTimeout(() => (this.loading = false), 2000);
    },
  },
};
</script>
