<template>
  <div class="wrapper">
    <parallax class="section page-header header-filter" :style="headerStyle">
      <div class="container">
        <div class="md-layout">
          <div
            class="md-layout-item md-size-50 md-small-size-70 md-xsmall-size-100"
          >
            <h1 class="title">Page 2 - To Test Routing.</h1>
           
          </div>
        </div>
      </div>
    </parallax>
    <div class="main main-raised">
      <div class="section">
        <div class="container">
          <div class="md-layout">
  
          </div>
       
        </div>
      </div>
      <div class="section text-center">
       
      </div>
      
    </div>
  </div>
</template>

<script>
export default {

  bodyClass: "test-page",
    props: {
    header: {
      type: String,
      default: require("@/assets/img/page2.jpg"),
    }},
  computed: {
    headerStyle() {
      return {
        backgroundImage: `linear-gradient(rgb(12 12 12 / 58%), rgb(3 4 3 / 72%)),  url(${this.header})`,
      };
    },
  },
};
</script>