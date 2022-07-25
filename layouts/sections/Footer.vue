<template>
  <!-- -----------------------------------------------
        Start Footer
  ----------------------------------------------- -->
  <v-footer class="footer">
    <v-container>
      <v-row class="py-0 ">
        <!-- -----------------------------------------------
        First Column
      ----------------------------------------------- -->
        <v-col cols="12" sm="12" md="12" lg="12" class="px-xs-0" style="text-align:center" >
          <h2 >小哈（宁波）科技有限公司</h2>
        </v-col>
        <v-col cols="12" sm="12" md="12" lg="4" class="px-xs-0">
          <h4 class="font-weight-regular font-18">地址 Address：</h4>
          <p class="mt-10">宁波鄞州区中河街道</p>
          <p>宁波保险科技产业园1号楼801</p>
        </v-col>
        <!-- -----------------------------------------------
        Second Column
      ----------------------------------------------- -->
        <v-col cols="12" sm="12" md="12" lg="4" class="px-xs-0">
          <h4 class="font-weight-regular font-18">电话 Tel：</h4>
          <p class="mt-10">0574-87919253</p>
        </v-col>
        <!-- -----------------------------------------------
        Third Column
      ----------------------------------------------- -->
        <v-col cols="12" sm="12" md="12" lg="4" class="px-xs-0">
          <h4 class="font-weight-regular font-18">邮箱 Email：
          </h4>
          <p class="mt-10 mb-0">xiaoha@healthappy365.com</p>
        </v-col>
        <!-- -----------------------------------------------
        Fourth Column
      ----------------------------------------------- -->
        <v-col cols="12" sm="12" md="12" lg="12" style="text-align:center;padding:0 !important"  class="px-xs-0">
          <img
              height="40"
              :src="require('@/assets/images/logo_white.png')"
              alt="logo"
            />
        </v-col>
      </v-row>
      <div class="footer-bottom-bar font-14">
        <div class="d-block d-md-flex justify-space-around">
          <p>
            <a href="https://beian.miit.gov.cn" class="link">浙ICP备19041095号-1</a>
          </p>
          <p class="ml-auto">
            Copyright &copy; 2017 - 2022 小哈（宁波）科技有限公司
          </p>
        </div>
      </div>
    </v-container>
  </v-footer>
  <!-- -----------------------------------------------
        End Footer
  ----------------------------------------------- -->
</template>

<script>
export default {
  name: "Footer",
  components: {},
  data() {
    return {
      data: [],
    };
  },
};
</script>
