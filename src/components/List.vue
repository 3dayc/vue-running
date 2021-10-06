<template>
  <v-card class="mx-auto" max-width="300" tile style="margin-bottom:50px">
    <v-list rounded>
      <v-subheader
        ><p>RUNNER(20)</p>
        <v-spacer></v-spacer>
        <p>누적km</p></v-subheader
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
              v-text="item.km"
              style="text-align:end"
            ></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    selectedItem: 0,
    items: [
      { text: "홍이", icon: "mdi-account", km: "5.7km" },
      { text: "향훈", icon: "mdi-account", km: "4.4km" },
      { text: "진혁", icon: "mdi-account", km: "3.4km" },
      { text: "박일광선", icon: "mdi-account", km: "2.1km" },
      { text: "성현", icon: "mdi-account", km: "1.1km" },
      { text: "고하늘", icon: "mdi-account", km: "0km" },
      { text: "김래오", icon: "mdi-account", km: "0km" },
      { text: "김예리", icon: "mdi-account", km: "0km" },
      { text: "김지훈", icon: "mdi-account", km: "0km" },
      { text: "용우", icon: "mdi-account", km: "0km" },
      { text: "이창명", icon: "mdi-account", km: "0km" },
      { text: "인우", icon: "mdi-account", km: "0km" },
      { text: "임연주", icon: "mdi-account", km: "0km" },
      { text: "전윤지", icon: "mdi-account", km: "0km" },
      { text: "종훈", icon: "mdi-account", km: "0km" },
      { text: "주미", icon: "mdi-account", km: "0km" },
      { text: "지원", icon: "mdi-account", km: "0km" },
      { text: "진수", icon: "mdi-account", km: "0km" },
      { text: "찬울", icon: "mdi-account", km: "0km" },
      { text: "향아", icon: "mdi-account", km: "0km" },
    ],
  }),
};
</script>
