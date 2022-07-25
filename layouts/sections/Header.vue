<template>
  <div>
    <!-- -----------------------------------------------
          Start Header
    ----------------------------------------------- -->
    <v-app-bar app class="app-header position-relative navbar-light  header1" flat>
      <v-container class="py-0 fill-height">
        <!-- Logo -->
        <div class="logo">
          <NLink to="/">
            <img
              height="50"
              :src="require('@/assets/images/logo_white.png')"
              alt="logo"
            />
          </NLink>
        </div>

        <v-spacer></v-spacer>
        <v-btn
          class="d-block d-md-none"
          text
          @click="toggleClass()"
        >
          <v-app-bar-nav-icon />
        </v-btn>
        <!-- Desktop view Navigation -->
        <div
          class="navigation"
          :class="[isActive ? 'd-block' : '']"
          @click="isActive = !isActive"
        >
          <ul class="navbar-nav">
            <v-menu v-for="(item,index) in navList" :key="index" offset-y>
              <template #activator="{ on, attrs }">
                <li class="nav-item" text>
                  <n-link v-if="item.children.length === 0" class="nav-link" nuxt :to="item.path">{{item.name}}</n-link>
                  <a v-else class="nav-link" href="#" v-bind="attrs" v-on="on">
                    {{item.name}}
                    <v-icon>mdi-chevron-double-down</v-icon>
                  </a>
                </li>
              </template>
              <v-list class="childMenu">
                <v-list-item v-for="(child, childIn) in item.children" :key="childIn" nav>
                  <n-link
                    style="text-decoration: none; color: #8c9295"
                    nuxt
                    :to="child.path"
                  >
                    {{child.name}}
                  </n-link>
                </v-list-item>
              </v-list>
            </v-menu>
          </ul>
        </div>
      </v-container>
    </v-app-bar>
    <!-- -----------------------------------------------
          End Header
    ----------------------------------------------- -->
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isActive: false,
      navList: [
        {
          name: "首页",
          path: "/",
          children: []
        },
        {
          name: "软件产品",
          path: "/software",
          children: [
            {
              name: "视光中心门诊SaaS",
              path: "/software/smartTown"
            },
            {
              name: "视力筛查系统",
              path: "/software/bigData"
            }
          ]
        },
        {
          name: "相关服务",
          path: "/service",
          children: []
        },
        {
          name: "公司介绍",
          path: "/newsinformation",
          children: []
        },
        // {
        //   name: "公司介绍",
        //   path: "/companyintroduction",
        //   children: []
        // },
        // {
        //   name: "工作机会",
        //   path: "/jobchance",
        //   children: []
        // },
        // {
        //   name: "联系我们",
        //   path: "/contactus",
        //   children: []
        // }
         {
          name: "软件产品",
          path: "/software",
          children: [
            {
              name: "视光中心门诊SaaS",
              path: "/software/smartTown"
            },
            {
              name: "视力筛查系统",
              path: "/software/bigData"
            }
          ]
        },
      ],
      items: [
        { title: "历史文件", link: "/history" },
        { title: "客户端下载" },
        { title: "Java 下载" },
      ],
    };
  },
  methods: {
    toggleClass: function () {
      this.isActive = !this.isActive;
    },
  },
};
</script>
<style scoped>
@media (max-width: 767px) {
  .v-menu__content{
    max-width: 100%;
    position: absolute;
    left: 0 !important;
    width: 100%;
    border-radius: 0;
  }
}
</style>
