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
            <a href="https://raiseguard.net/" target="_blank"> raiseguard </a>
          </li>
          <li>
            <a href=""> About Us </a>
          </li>
          <li>
            <router-link to="/contact">Contact Us</router-link>
          </li>
        </ul>
      </nav>
      <div class="copyright">
        &copy; {{ year }},
        <a class="category category-absolute">
          Designed by &nbsp;
          <a href="https://raiseguard.net/" target="_blank">
            <img src="img/RG.png" class="invision-logo" /> &nbsp; </a
          >.
        </a>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String,
  },
  data() {
    return {
      year: new Date().getFullYear(),
    };
  },
};
</script>
<style></style>
