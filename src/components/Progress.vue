<template>
  <div style="width:350px; margin:0 auto 48px">
    <h3 style="text-align:center; margin-bottom:20px">
      <span style="color:#212121;">0</span>
      <span style="color:#757575;"> / 100 km</span>
    </h3>
    <v-progress-linear
      buffer-value="0"
      value="0"
      stream
      color="orange"
    ></v-progress-linear>
  </div>
</template>
