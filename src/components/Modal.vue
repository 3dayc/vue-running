<template>
  <v-row justify="space-around" style="margin-top:36px;">
    <!-- <v-col cols="auto">
      <v-dialog transition="dialog-bottom-transition" max-width="600">
        <template v-slot:activator="{ on, attrs }">
          <v-btn color="primary" v-bind="attrs" v-on="on"
            >From the bottom</v-btn
          >
        </template>
        <template v-slot:default="dialog">
          <v-card>
            <v-toolbar color="primary" dark>Opening from the bottom</v-toolbar>
            <v-card-text>
              <div class="text-h2 pa-12">Hello world!</div>
            </v-card-text>
            <v-card-actions class="justify-end">
              <v-btn text @click="dialog.value = false">Close</v-btn>
            </v-card-actions>
          </v-card>
        </template>
      </v-dialog>
    </v-col> -->

    <v-col cols="auto">
      <v-dialog transition="dialog-top-transition" max-width="600">
        <template v-slot:activator="{ on, attrs }">
          <v-btn color="primary" v-bind="attrs" v-on="on">Click</v-btn>
        </template>
        <template v-slot:default="dialog">
          <v-card>
            <v-toolbar color="primary" dark>테스트 페이지 (미완성)</v-toolbar>
            <v-card-text>
              <div class="text-h6 pa-12">
                1차 정기 이벤트<br />
                <p style="font-size:14px; margin-top:10px">
                  * 10/16~10/30 기간 동안의 누적km 기록<br />
                  * 3등까지 소정의 상품 증정<br />
                  * 나이키런, 가민 등 기록 캡처본을 러닝 단톡방에 올린것만
                  인정<br />
                  * 메인 프로필은 기록 업데이트 시 선두 프로필로 변경
                </p>
              </div>
            </v-card-text>
            <v-card-actions class="justify-end">
              <v-btn text @click="dialog.value = false">Close</v-btn>
            </v-card-actions>
          </v-card>
        </template>
      </v-dialog>
    </v-col>
  </v-row>
</template>
