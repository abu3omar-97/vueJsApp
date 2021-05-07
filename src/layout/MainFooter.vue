<template>
  <footer
    class="footer"
    :class="{ [`footer-${type}`]: type }"
    :data-background-color="backgroundColor"
  >
    <div class="container">
      <nav>
        <ul>
          <li>
            <a href="https://">
              Home
            </a>
          </li>
          <li>
            <a href="">
              About Us
            </a>
          </li>
          <li>
            <a href="">
              Products
            </a>
          </li>
        </ul>
      </nav>
      <div class="copyright">
        &copy; {{ year }},  by
        <a href="" target="_blank">Yaman Alashqar</a>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String
  },
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style></style>
