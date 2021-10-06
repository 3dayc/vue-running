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
            <v-toolbar color="primary" dark>알림창</v-toolbar>
            <v-card-text>
              <div class="text-h6 pa-12">
                10월 100km 가을 챌린지<br />
                <ul style="font-size:14px; margin-top:20px">
                  <li>
                    10/09~10/30(3주) 간 개인 누적 합산 100km 달성하기 [팀미션]
                  </li>
                  <li>챌린지 기여km 3등까지 소정의 상품 증정 [개인미션]</li>
                  <li>
                    나이키런, 가민 등 기록 캡처본을 러닝 톡방에 올린것만 공식
                    인정
                  </li>
                  <li>
                    메인 프로필은 기록 업데이트 당시 선두 러너의 프로필로 수시
                    변경
                  </li>
                  <li>기록 업데이트는 1~2일에 한번 사이트 관리자가 진행</li>
                </ul>
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
