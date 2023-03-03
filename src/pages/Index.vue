<template>
  <div>
    <div class="page-header clear-filter" filter-color="orange">
      <parallax
        class="page-header-image"
        style="background-image:url('img/Cybersecurity.jpg')"
      >
      </parallax>
      <div class="container">
        <div class="content-center brand">
          <img class="n-logo" src="img/Logo_Security.png" alt="" />
          <h1 class="h1-seo">SOC platform</h1>
          <h3>we provide security with the necessary tools to monitor, detect, and respond to cyber threats in real-time.</h3>
        </div>
        <h6 class="category category-absolute">
          Designed by
          <a href="https://www.defensy.io/" target="_blank">
            <img src="img/DefensyLogo.png" class="invision-logo" /> </a
          >
          <!-- . Coded by
          <a href="https://www.creative-tim.com" target="_blank">
            <img
              src="img/creative-tim-white-slim2.png"
              class="creative-tim-logo"
            /> </a
          >. -->
        </h6>
      </div>
    </div>
    <div class="main">
      <div class="section section-images">
        <div class="container">
          <div class="row">
            <div class="col-md-12">
              <div class="hero-images-container">
                <img src="img/hero-image-1.png" alt="" />
              </div>
              <div class="hero-images-container-1">
                <img src="img/hero-image-2.png" alt="" />
              </div>
              <div class="hero-images-container-2">
                <img src="img/hero-image-3.png" alt="" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- <basic-elements></basic-elements>
    <navigation></navigation>
    <tabs-section></tabs-section>
    <progress-pagination></progress-pagination>
    <notifications></notifications>
    <typography></typography>
    <javascript-components></javascript-components>
    <carousel-section></carousel-section>
    <nucleo-icons-section></nucleo-icons-section> -->
    <div class="section">
      <div class="container text-center">
        <div class="row justify-content-md-center">
          <div class="col-md-12 col-lg-12">
            <h2 class="title">Select Your Service Plan</h2>
            <Plans />
          </div>
        </div>
      </div>
    </div>
    <carousel :items="4" :margin="10" :autoplay="true" :mouseDrag="true" :stagePadding="50" :dots="true" :autoplayHoverPause="true">
          <div class="slider-card">
						<div class="d-flex justify-content-center align-items-center mb-4">
							<img src="../../src/assets/images/slide-1.jpg" alt="" >
						</div>
						<h5 class="mb-0 text-center"><b>Threat intelligence</b></h5>
						<p class="text-center p-4">A SOC should have access to the latest threat intelligence data, which can help identify potential security threats and vulnerabilities.</p>
					</div>
					<div class="slider-card">
						<div class="d-flex justify-content-center align-items-center mb-4">
							<img src="../../src/assets/images/slide-2.jpg" alt="">
						</div>
						<h5 class="mb-0 text-center"><b>Security information and event management (SIEM)</b></h5>
						<p class="text-center p-4">A SIEM system is used to collect and analyze security event data from various sources within the organization's network. This can help detect security incidents in real-time and provide insights for improving security posture.</p>
					</div>
					<div class="slider-card">
						<div class="d-flex justify-content-center align-items-center mb-4">
							<img src="../../src/assets/images/slide-3.jpg" alt="">
						</div>
						<h5 class="mb-0 text-center"><b>Incident response</b></h5>
						<p class="text-center p-4">A SOC should have a documented incident response plan in place that outlines the steps that should be taken in the event of a security breach or incident. This includes procedures for containment, investigation, and recovery.</p>
					</div>
					<div class="slider-card">
						<div class="d-flex justify-content-center align-items-center mb-4">
							<img src="../../src/assets/images/slide-4.jpg" alt="">
						</div>
						<h5 class="mb-0 text-center"><b>Monitoring and analysis</b></h5>
						<p class="text-center p-4">The SOC should have a team of analysts who are responsible for monitoring the network for potential security threats and analyzing security event data to identify patterns and trends.</p>
					</div>
          <div class="slider-card">
						<div class="d-flex justify-content-center align-items-center mb-4">
							<img src="../../src/assets/images/slide-5.jpg" alt="">
						</div>
						<h5 class="mb-0 text-center"><b>Threat hunting</b></h5>
						<p class="text-center p-4">The SOC team should also proactively search for potential security threats that may not have been detected by automated monitoring systems.</p>
					</div>
					<div class="slider-card">
						<div class="d-flex justify-content-center align-items-center mb-4">
							<img src="../../src/assets/images/slide-6.jpg" alt="">
						</div>
						<h5 class="mb-0 text-center"><b>Forensics and investigations</b></h5>
						<p class="text-center p-4"> If a security breach does occur, the SOC should have the tools and expertise necessary to conduct a forensic investigation to determine the cause and scope of the breach.</p>
					</div>
          <div class="slider-card">
						<div class="d-flex justify-content-center align-items-center mb-4">
							<img src="../../src/assets/images/slide-1.jpg" alt="">
						</div>
						<h5 class="mb-0 text-center"><b>Communication and reporting</b></h5>
						<p class="text-center p-4">The SOC should communicate with stakeholders across the organization to keep them informed about security threats and incidents. They should also provide regular reports on security metrics and trends to senior management.</p>
					</div>
          <div class="slider-card">
						<div class="d-flex justify-content-center align-items-center mb-4">
							<img src="../../src/assets/images/slide-2.jpg" alt="">
						</div>
						<h5 class="mb-0 text-center"><b>Continuous improvement</b></h5>
						<p class="text-center p-4">The SOC should be committed to continuous improvement, regularly reviewing and updating their processes, procedures, and technologies to stay ahead of evolving security threats.</p>
					</div>
          
</carousel>
    <!-- <signup-form></signup-form>
    <examples-section></examples-section>
    <download-section></download-section> -->
  </div>
</template>
<script>
import { Parallax } from '@/components';
import BasicElements from './components/BasicElementsSection';
import Navigation from './components/Navigation';
import TabsSection from './components/Tabs';
import ProgressPagination from './components/ProgressPagination';
import Notifications from './components/Notifications';
import Typography from './components/Typography';
import JavascriptComponents from './components/JavascriptComponents';
import CarouselSection from './components/CarouselSection';
import NucleoIconsSection from './components/NucleoIconsSection';
import SignupForm from './components/SignupForm';
import ExamplesSection from './components/ExamplesSection';
import DownloadSection from './components/DownloadSection';
import Plans from './components/Plans';
import carousel from 'vue-owl-carousel'

export default {
  name: 'index',
  bodyClass: 'index-page',
  components: {
    // Parallax,
    // BasicElements,
    // Navigation,
    // TabsSection,
    // ProgressPagination,
    // Notifications,
    // Typography,
    // JavascriptComponents,
    // CarouselSection,
    // NucleoIconsSection,
    // SignupForm,
    // ExamplesSection,
    // DownloadSection
    Plans,
    carousel 
  }
};
</script>
<style></style>
