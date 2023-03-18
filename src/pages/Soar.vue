<template>
  <div>
    <div class="page-header clear-filter" filter-color="orange">
      <div
        class="page-header-image"
        style="background-image: url('img/bg3.jpg')"
      ></div>
      <div class="content-center row">
        <div class="colcol-6">
          <img height="250" src="img/soar.png" alt="" />
        </div>
        <div class="col-6">
          <h2 class="font-weight-bold">Notifications.</h2>
          NIST CSF
          <span class="id-color-2">RS.CO-3:</span>
          Information is shared consistent with response plans. <br />
        </div>
        <div class="col-6">
          <h2 class="font-weight-bold">Workflows and Orchestration.</h2>
          NIST CSF
          <span class="id-color-2">RS.CO-2:</span>
          Incidents are reported consistent with established criteria.
        </div>
        <div class="col-md-12 text-center">
          <button type="button" class="btn btn-primary" @click="scroll()">
            Show me more
          </button>
        </div>
      </div>
    </div>
    <div
      class="container position-relative"
      style="margin-top: -25vh; position: absolute"
    >
      <div class="hero-images-container d-flex justify-content-center">
        <img src="img/laptop.png" alt="" />
      </div>
    </div>
    <div>
      <!-- <div class="container" id="scroll">
        <div class="">
          <div class="card" style="width: 18rem">
            <div class="card-body">
              <h5 class="card-title">Workflows.</h5>
              <br />
              <p class="card-text">
                Workflows are made using a varitety of frameworks and tools.
              </p>
            </div>
          </div>
          <div class="card" style="width: 18rem">
            <div class="card-body">
              <h5 class="card-title">Orchestration and Playbooks</h5>
              <p class="card-text">
                SOCFortress crafts playbooks to orchestrate full response
                chains.
              </p>
            </div>
          </div>
          <div class="card" style="width: 18rem">
            <div class="card-body">
              <h5 class="card-title">Orchestrated Response.</h5>
              <br />
              <p class="card-text">
                Playbooks integrate different actions and targets.
              </p>
              <br />
            </div>
          </div>
          <div class="card" style="width: 18rem">
            <div class="card-body">
              <h5 class="card-title">Artifacts Collection.</h5>
              <p class="card-text">
                Playbooks execution can extend beyond the affected asset,
                collecting additional artifacts.
              </p>
            </div>
          </div>
          <div class="card" style="width: 18rem">
            <div class="card-body">
              <h5 class="card-title">User Notifications.</h5>
              <p class="card-text">
                Different communication channels available as part of the
                orchestrated response.
              </p>
            </div>
          </div>
        </div>
      </div> -->
      <div class="container" id="scroll">
        <div class="row">
          <div class="col-md-4 mt-5">
            <div class="card">
              <div class="circle">
                <i class="fa fa-wrench"></i>
              </div>
              <div class="card-body">
                <h5 class="card-title text-center">Workflows</h5>
                <p class="card-text">
                  Workflows are made using a varitety of frameworks and tools.
                </p>
              </div>
            </div>
          </div>
          <div class="col-md-4 mt-5">
            <div class="card">
              <div class="circle circle1">
                <i class="fa fa-globe"></i>
              </div>
              <div class="card-body">
                <h5 class="card-title text-center">
                  Orchestration and Playbooks
                </h5>
                <p class="card-text">
                  SOC platform crafts playbooks to orchestrate full response
                  chains.
                </p>
              </div>
            </div>
          </div>
          <div class="col-md-4 mt-5">
            <div class="card">
              <div class="circle circle3">
                <i class="fa fa-laptop"></i>
              </div>
              <div class="card-body">
                <h5 class="card-title text-center">Orchestrated Response</h5>
                <p class="card-text">
                  Playbooks integrate different actions and targets.
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-md-4 mt-5">
            <div class="card">
              <div class="circle circle4">
                <i class="fa fa-file"></i>
              </div>
              <div class="card-body">
                <h5 class="card-title text-center">Artifacts Collection</h5>
                <p class="card-text">
                  Playbooks execution can extend beyond the affected asset,
                  collecting additional artifacts.
                </p>
              </div>
            </div>
          </div>
          <div class="col-md-4 mt-5">
            <div class="card">
              <div class="circle circle5">
                <i class="fa fa-user"></i>
              </div>
              <div class="card-body">
                <h5 class="card-title text-center">User Notifications</h5>
                <p class="card-text">
                  Different communication channels available as part of the
                  orchestrated response.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="container text-center font-weight-bold">
        <h2 style="color: blue">SOAR</h2>
        <h3>Security Orchestration, Automation amd Response.</h3>
      </div>
      <div class="accordion  container " id="accordionFlushExample">
        <div class="accordion-item">
          <h2 class="accordion-header" id="flush-headingOne">
            <button
              class="accordion-button collapsed"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#flush-collapseOne"
              aria-expanded="false"
              aria-controls="flush-collapseOne"
            >
              Plugins and Integrations.
            </button>
          </h2>
          <div
            id="flush-collapseOne"
            class="accordion-collapse collapse"
            aria-labelledby="flush-headingOne"
            data-bs-parent="#accordionFlushExample"
          >
            <div class="accordion-body">
              <img class="imgshow" height="250" src="img/soar1.png" alt="" />
            </div>
          </div>
        </div>
        <div class="accordion-item">
          <h2 class="accordion-header" id="flush-headingTwo">
            <button
              class="accordion-button collapsed"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#flush-collapseTwo"
              aria-expanded="false"
              aria-controls="flush-collapseTwo"
            >
              Workflows.
            </button>
          </h2>
          <div
            id="flush-collapseTwo"
            class="accordion-collapse collapse"
            aria-labelledby="flush-headingTwo"
            data-bs-parent="#accordionFlushExample"
          >
            <div class="accordion-body">
              <img class="imgshow" height="250" src="img/soar2.png" alt="" />
            </div>
          </div>
        </div>
        <div class="accordion-item">
          <h2 class="accordion-header" id="flush-headingThree">
            <button
              class="accordion-button collapsed"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#flush-collapseThree"
              aria-expanded="false"
              aria-controls="flush-collapseThree"
            >
              Apps Ecosystem.
            </button>
          </h2>
          <div
            id="flush-collapseThree"
            class="accordion-collapse collapse"
            aria-labelledby="flush-headingThree"
            data-bs-parent="#accordionFlushExample"
          >
            <div class="accordion-body">
              <img class="imgshow" height="250" src="img/soar3.png" alt="" />
            </div>
          </div>
        </div>
      </div>
      <div class="container">
        <h4>Multiple apps out of the box and many more that we craft to cover all integration needs.</h4>
      </div>
      <br />
      <br />
      <br />
    </div>
  </div>
</template>
<script>
import Button from "../components/Button.vue";
export default {
  name: "index",
  //data for typewriter
  setup() {
    return {
      toggle1: false,
      toggle2: true,
      toggle3: true,
    };
  },
  data: () => {
    return {
      typeValue: "",
      typeStatus: false,
      displayTextArray: ["Prevention", "Detection", "Response"],
      typingSpeed: 70,
      erasingSpeed: 70,
      newTextDelay: 700,
      displayTextArrayIndex: 0,
      charIndex: 0,
    };
  },
  created() {
    setTimeout(this.typeText, this.newTextDelay + 200);
  },
  methods: {
    scroll() {
      const element = document.getElementById("scroll");
      element.scrollIntoView({ behavior: "smooth" });
    },
    typeText() {
      if (
        this.charIndex <
        this.displayTextArray[this.displayTextArrayIndex].length
      ) {
        if (!this.typeStatus) this.typeStatus = true;
        this.typeValue += this.displayTextArray[
          this.displayTextArrayIndex
        ].charAt(this.charIndex);
        this.charIndex += 1;
        setTimeout(this.typeText, this.typingSpeed);
      } else {
        this.typeStatus = false;
        setTimeout(this.eraseText, this.newTextDelay);
      }
    },
    eraseText() {
      if (this.charIndex > 0) {
        if (!this.typeStatus) this.typeStatus = true;
        this.typeValue = this.displayTextArray[
          this.displayTextArrayIndex
        ].substring(0, this.charIndex - 1);
        this.charIndex -= 1;
        setTimeout(this.eraseText, this.erasingSpeed);
      } else {
        this.typeStatus = false;
        this.displayTextArrayIndex += 1;
        if (this.displayTextArrayIndex >= this.displayTextArray.length)
          this.displayTextArrayIndex = 0;
        setTimeout(this.typeText, this.typingSpeed + 1000);
      }
    },
  },
  // till here typewriter
  bodyClass: "index-page",
};
import "./Soar.css";
</script>

<style lang="scss" scoped>
#scroll {
  scroll-margin-top: 100px;
}
.imgshow {
  width: 100%;
  height: 500px;
  background-repeat: no-repeat;
  background-size: contain;
}
</style>
