<template>
  <div class="feature3-component mini-spacer">
    <v-container class="position-relative">
      <!-- -----------------------------------------------
          Start Feature 3 Text
      ----------------------------------------------- -->
      <v-row>
        <v-col cols="12" lg="10">
          <v-img
            :src="require('@/assets/images/banner/sys.png')"
            alt="feature"
            class="rounded"
          />
        </v-col>
        <v-col cols="12" md="7" lg="5" class="feature3-card">
          <v-card class="card-shadow border-all">
            <v-card-text>
              <div class="pa-10 text-center">
                <h3 class="feature3-title font-weight-medium">
                  视光门诊SaaS系统
                </h3>
                <h4 class="feature3-title-en">
                  Optometry clinic SaaS system
                </h4>
                <p class="text-left">
                  当今最领先的眼健康平台。
                  我们保证不做影响平衡、破坏公平的行为。服务器开放白名单以及正版验证，欢迎玩家提出意见或者举报违规行为，请大家自觉遵守游戏规则。
                </p>
              </div>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>

      <!-- -----------------------------------------------
          End Feature 3 Text
      ----------------------------------------------- -->
    </v-container>
  </div>
</template>
<script>
import { getImage } from "assets/images/getImg";

export default {
  name: "Feature3",
  data() {
    return {
      getImage,
    };
  },
  methods: {},
};
</script>
