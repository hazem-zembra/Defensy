<template>
  <navbar
    position="fixed"
    type="primary"
    :transparent="transparent"
    :color-on-scroll="colorOnScroll"
    menu-classes="ml-auto"
  >
    <template>
      <a href="https://www.defensy.io/" target="_blank">
            <img src="img/DefensyLogoW.png" class="img" /> </a>
      <el-popover
        ref="popover1"
        popper-class="popover"
        placement="bottom"
        width="200"
        trigger="hover"
      >
        <div class="popover-body">
          Designed by DefensyLab
        </div>
      </el-popover>
    </template>
    <template slot="navbar-menu">
      <li class="nav-item">
        <a
          class="nav-link"
          href=""
          target="_blank"
        >
          <i class="now-ui-icons shopping_shop"></i>
          <p>Home</p>
        </a>
      </li>

      <li class="nav-item">
        <a
          class="nav-link"
          href=""
          target="_blank"
        >
          <i class="now-ui-icons business_bulb-63"></i>
          <p>About us</p>
        </a>
      </li>

      <li class="nav-item">
        <a
          class="nav-link"
          href=""
          target="_blank"
        >
          <i class="now-ui-icons ui-1_email-85"></i>
          <p>Contact us</p>
        </a>
      </li>

      <!-- uncomment dropdown and nav link in components down below too -->
      <!-- <drop-down
        tag="li"
        title="Components"
        icon="now-ui-icons design_app"
        class="nav-item"
      >
        <nav-link to="/">
          <i class="now-ui-icons business_chart-pie-36"></i> All components
        </nav-link>
        <a
          href="https://demos.creative-tim.com/vue-now-ui-kit/documentation"
          target="_blank"
          class="dropdown-item"
        >
          <i class="now-ui-icons design_bullet-list-67"></i> Documentation
        </a>
      </drop-down>
      <drop-down
              tag="li"
              title="Examples"
              icon="now-ui-icons design_image"
              class="nav-item"
      >
        <nav-link to="/landing">
          <i class="now-ui-icons education_paper"></i> Landing
        </nav-link>
        <nav-link to="/login">
          <i class="now-ui-icons users_circle-08"></i> Login
        </nav-link>
        <nav-link to="/profile">
          <i class="now-ui-icons users_single-02"></i> Profile
        </nav-link>
      </drop-down> -->
      <li class="nav-item">
        <a
          class="nav-link btn btn-success"
          href="https://www.creative-tim.com/product/vue-now-ui-kit-pro"
          target="_blank"
        >
          <i class="now-ui-icons media-1_button-play"></i>
          <p>&nbsp; Live Demo</p>
        </a>
      </li>

      <li class="nav-item">
        <a
          class="nav-link"
          rel="tooltip"
          title="Our Official Website"
          data-placement="bottom"
          href="https://www.defensy.io/"
          target="_blank">
          <i class="now-ui-icons objects_globe"></i>
          <p class="d-lg-none d-xl-none">Website</p>
        </a>
      </li>

      <li class="nav-item">
        <a
          class="nav-link"
          rel="tooltip"
          title="Like us on facebook"
          data-placement="bottom"
          href="https://www.facebook.com/Defensy/"
          target="_blank">
          <i class="fab fa-facebook-square"></i>
          <p class="d-lg-none d-xl-none">Facebook</p>
        </a>
      </li>

      <li class="nav-item">
        <a
          class="nav-link"
          rel="tooltip"
          title="Follow us on Linkedin"
          data-placement="bottom"
          href="https://www.linkedin.com/company/defensy/"
          target="_blank">
          <i class="fab fa-linkedin"></i>
          <p class="d-lg-none d-xl-none">Linkedin</p>
        </a>
      </li>
      
      
    </template>
  </navbar>
</template>

<script>
import { DropDown, Navbar, NavLink } from '@/components';
import { Popover } from 'element-ui';
export default {
  name: 'main-navbar',
  props: {
    transparent: Boolean,
    colorOnScroll: Number
  },
  components: {
    // DropDown,
    Navbar,
    // NavLink,
    [Popover.name]: Popover
  }
};
</script>

<style scoped>

.img{width: 150px}
</style>
