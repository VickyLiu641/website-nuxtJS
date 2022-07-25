<template>
  <v-main>
    <div class="banner-wrapper" style="background-color: #DE5D5D">
      <v-container>
        <v-row justify="center">
          <v-col cols="12" sm="10" md="6" lg="4" class="d-flex align-center justify-center">
            <div class="text-center">
              <h1 class="banner-title font-weight-bold white--text">Sorry, 404 - Error</h1>
              <h4 class="banner-subtitle mr-0 white--text font-weight-regular">
                The page you are looking for is not available please go back to homepage
              </h4>
              <div class="mt-16 pt-2">
                <v-btn nuxt large to="/" color="error" elevation="0">Back to Homepage</v-btn>
              </div>
            </div>
          </v-col>
        </v-row>
        </v-container>
      </div>
  </v-main>
</template>

<script>
export default {
  layout: "empty",
  props: {
    error: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {
      pageNotFound: "404 Not Found",
      otherError: "An error occurred",
    };
  },
  head() {
    const title = this.error.statusCode === 404 ? this.pageNotFound : this.otherError;
    return {
      title,
    };
  },
};
</script>

<style scoped>
h1 {
  font-size: 20px;
}
</style>
