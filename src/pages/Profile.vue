<template>
  <div>
    <div class="page-header clear-filter" filter-color="orange">
      <parallax
        class="page-header-image"
        style="background-image:url('img/About.jpg')"
      >
      </parallax>
      <div class="container">
        <div class="photo-container">
          <img src="img/Logo_Security.png" alt="" />
        </div>
        <h3 class="title">RAISEGUARD SOC Platform</h3>
        <p class="category"></p>
        <div class="content">
          <div class="social-description">
            <h2>+{{ count_visitors }}{{ number_abbreviation_visitors }}</h2>
            <p>Total Visitors/Day</p>
          </div>
          <div class="social-description">
            <h2>+570</h2>
            <p>Interactions</p>
          </div>
          <div class="social-description">
            <h2>+152K</h2>
            <p>Social Media followers </p>
          </div>
        </div>
      </div>
    </div>
    <div class="section">
      <div class="container">
        <div class="button-container">
          <a href="https://raiseguard.net/" class="btn btn-primary btn-round btn-lg"><i class="fa fa-globe"></i> Visit us</a>
          <a
            href="https://www.linkedin.com/company/raiseguard/  "
            class="btn btn-default btn-round btn-lg btn-icon"
            rel="tooltip"
            title="Follow me on LinkedIn"
          >
            <i class="fab fa-linkedin"></i>
          </a>
          <!-- <a
            href="#button"
            class="btn btn-default btn-round btn-lg btn-icon"
            rel="tooltip"
            title="Follow me on Facebook"
          >
            <i class="fab fa-facebook-square"></i>
          </a> -->
        </div>
        <h3 class="title">About us</h3>
        <h5 class="description">
         A hub for cybersecurity operations and threat management. It provides real-time monitoring, detection, and response to security incidents.
        We offer dashboards, visualizations, and other functionalities to provide SOC analysts with real-time visibility into network activity and potential threats. 
        </h5>
        <!-- <div class="row">
          <div class="col-md-6 ml-auto mr-auto">
            <h4 class="title text-center">My Portfolio</h4>
          </div>
          <tabs
            pills
            class="nav-align-center"
            tab-content-classes="gallery"
            tab-nav-classes="nav-pills-just-icons"
            type="primary"
          >
            <tab-pane title="Profile">
              <i slot="label" class="now-ui-icons design_image"></i>

              <div class="col-md-10 ml-auto mr-auto">
                <div class="row collections">
                  <div class="col-md-6">
                    <img src="img/bg6.jpg" class="img-raised" />
                    <img src="img/bg11.jpg" alt="" class="img-raised" />
                  </div>
                  <div class="col-md-6">
                    <img src="img/bg7.jpg" alt="" class="img-raised" />
                    <img src="img/bg8.jpg" alt="" class="img-raised" />
                  </div>
                </div>
              </div>
            </tab-pane>

            <tab-pane title="Home">
              <i slot="label" class="now-ui-icons location_world"></i>

              <div class="col-md-10 ml-auto mr-auto">
                <div class="row collections">
                  <div class="col-md-6">
                    <img src="img/bg1.jpg" alt="" class="img-raised" />
                    <img src="img/bg3.jpg" alt="" class="img-raised" />
                  </div>
                  <div class="col-md-6">
                    <img src="img/bg8.jpg" alt="" class="img-raised" />
                    <img src="img/bg7.jpg" alt="" class="img-raised" />
                  </div>
                </div>
              </div>
            </tab-pane>

            <tab-pane title="Messages">
              <i slot="label" class="now-ui-icons sport_user-run"></i>

              <div class="col-md-10 ml-auto mr-auto">
                <div class="row collections">
                  <div class="col-md-6">
                    <img src="img/bg3.jpg" alt="" class="img-raised" />
                    <img src="img/bg8.jpg" alt="" class="img-raised" />
                  </div>
                  <div class="col-md-6">
                    <img src="img/bg7.jpg" alt="" class="img-raised" />
                    <img src="img/bg6.jpg" class="img-raised" />
                  </div>
                </div>
              </div>
            </tab-pane>
          </tabs>
        </div> -->
      </div>
    </div>
  </div>
</template>
<script>
import { Tabs, TabPane } from '@/components';

export default {
  name: 'profile',
  bodyClass: 'profile-page',
  // components: {
  //   Tabs,
  //   TabPane
  // }
  data() {
    return {
      count_visitors: 0,
      count_interactions: 0 ,
      count_followers: 0,
      total_visitors: 185250,
      intervalId: null,
      number_abbreviation_visitors : ''
    };
  },
  mounted() {
    this.intervalId = setInterval(() => {
      if (this.total_visitors > 1000){
        var counter = Math.trunc(this.total_visitors / 1000);;
        this.number_abbreviation_visitors = 'K';
          if(counter > 1000){
            var counter = Math.trunc(counter / 1000);
            this.number_abbreviation_visitors = 'M';
          }
        this.count_visitors++;
      if (this.count_visitors === counter) {
        clearInterval(this.intervalId);
      }
      }
    }, 1);
  }
};
</script>
<style></style>
