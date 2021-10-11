<template>
  <div>
    <Progress :sum="sum" />
    <v-card class="mx-auto" max-width="300" tile style="margin-bottom:50px">
      <v-list rounded>
        <v-subheader
          ><p>RUNNER(20)</p>
          <v-spacer></v-spacer>
          <p>기여km</p></v-subheader
        >
        <v-list-item-group v-model="selectedItem" color="primary">
          <v-list-item v-for="(item, i) in items" :key="i">
            <v-list-item-icon>
              <v-icon v-text="item.icon"></v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item-content>
            <v-list-item-content>
              <v-list-item-title
                v-text="item.km + 'km'"
                style="text-align:end"
              ></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-card>
  </div>
</template>

<script>
import Progress from "./Progress";

export default {
  components: {
    Progress,
  },

  data: () => ({
    selectedItem: 0,
    items: [
      { text: "지원", icon: "mdi-account", km: 6.94 },
      { text: "용우", icon: "mdi-account", km: 6.21 },
      { text: "종훈", icon: "mdi-account", km: 5.06 },
      { text: "향훈", icon: "mdi-account", km: 5.06 },
      { text: "홍이", icon: "mdi-account", km: 5 },
      { text: "고하늘", icon: "mdi-account", km: 0 },
      { text: "진혁", icon: "mdi-account", km: 0 },
      { text: "박일광선", icon: "mdi-account", km: 0 },
      { text: "성현", icon: "mdi-account", km: 0 },
      { text: "김래오", icon: "mdi-account", km: 0 },
      { text: "김예리", icon: "mdi-account", km: 0 },
      { text: "김지훈", icon: "mdi-account", km: 0 },
      { text: "이창명", icon: "mdi-account", km: 0 },
      { text: "인우", icon: "mdi-account", km: 0 },
      { text: "임연주", icon: "mdi-account", km: 0 },
      { text: "전윤지", icon: "mdi-account", km: 0 },
      { text: "주미", icon: "mdi-account", km: 0 },
      { text: "진수", icon: "mdi-account", km: 0 },
      { text: "찬울", icon: "mdi-account", km: 0 },
      { text: "향아", icon: "mdi-account", km: 0 },
    ],
  }),

  computed: {
    sum() {
      let total_km = 0;
      for (let i = 0; i < this.items.length; i++) {
        total_km = total_km + this.items[i].km;
      }
      return total_km;
    },
  },
};
</script>
