<template>
  <v-app dark>
    <Header />
    <v-main>
      <nuxt />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
export default {
  components: {
    Footer: () => import("@/layouts/sections/Footer"),
    Header: () => import("@/layouts/sections/Header"),
  },
  head() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss">
::-webkit-scrollbar {
  width: 10px; /*竖向滚动条的宽度*/
  height: 10px; /*横向滚动条的高度*/
}

::-webkit-scrollbar-thumb { /*滚动条里面的小方块*/
  background: #8DD7F7;
  border-radius: 5px;
}

::-webkit-scrollbar-track { /*滚动条轨道的样式*/
  background: #ccc;
  border-radius: 5px;
}
</style>
