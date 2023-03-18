<template>
  <div>
    <div class="page-header clear-filter" filter-color="orange">
      <div
        class="page-header-image"
        style="background-image: url('img/bg3.jpg')"
      ></div>
      <br />
      <div class="content-center row">
        <div class="colcol-6">
          <img height="250" src="img/soar.png" alt="" />
        </div>
        <div class="col-6">
          <br />
          <h2 style="font-weight: bold">Notifications.</h2>
          NIST CSF
          <span class="id-color-2">RS.CO-3:</span>
          Information is shared consistent with response plans. <br />
          <div>
            <button href="middle" type="button" class="btn btn-primary">
              Show me more
            </button>
          </div>
        </div>
        <div class="col-6">
          <h2 style="font-weight: bold">Workflows and Orchestration.</h2>
          NIST CSF
          <span class="id-color-2">RS.CO-2:</span>
          Incidents are reported consistent with established criteria.
          <div>
            <button type="button" class="btn btn-primary">Show me more</button>
          </div>
        </div>
      </div>
    </div>
    <br />
    <div>
      <div class="position-relative section-images">
        <div class="container">
          <br />
          <div class="row justify-content-center">
            <div class="hero-images-container">
              <br />
              <img src="img/laptop.png" alt="" />
            </div>

            <ul
              class="position-relative list-group list-group-horizontal-sm row"
            >
              <li class="col-md-3">
                <div id="middle" class="stat-card">
                  <a href="#middle"></a>
                  <div class="stat-icon right">
                    <span class="bg-measure house"></span><i class="house"></i>
                  </div>
                  <h2 style="font-weight: bold">Workflows.</h2>
                  <br />
                  <h4 class="stat-num"></h4>
                  <div class="subtext">
                    <i class="glyphicon glyphicon-triangle-top txt-ontrack"></i>
                    Workflows are made using a varitety of frameworks and tools.
                  </div>
                </div>
              </li>

              <li class="col-md-3">
                <div class="stat-card">
                  <div class="stat-icon right">
                    <span class="bg-measure users_single-02"></span
                    ><i class="glyphicon glyphicon-home"></i>
                  </div>
                  <h2 style="font-weight: bold">
                    Orchestration and Playbooks.
                  </h2>
                  <h4 class="stat-num"></h4>
                  <div class="subtext">
                    <i class="glyphicon glyphicon-triangle-top txt-ontrack"></i>
                    SOCFortress crafts playbooks to orchestrate full response
                    chains.
                  </div>
                </div>
              </li>
              <li class="col-md-3">
                <div class="stat-card">
                  <div class="stat-icon right">
                    <span class="bg-measure users_single-02"></span
                    ><i class="glyphicon glyphicon-home"></i>
                  </div>
                  <h2 style="font-weight: bold">Orchestrated Response.</h2>
                  <h4 class="stat-num"></h4>
                  <div class="subtext">
                    <i class="glyphicon glyphicon-triangle-top txt-ontrack"></i>
                    Playbooks integrate different actions and targets.
                  </div>
                </div>
              </li>
              <li class="col-md-3">
                <div class="stat-card">
                  <div class="stat-icon right">
                    <span class="bg-measure users_single-02"></span
                    ><i class="glyphicon glyphicon-home"></i>
                  </div>
                  <h2 style="font-weight: bold">Artifacts Collection.</h2>
                  <h4 class="stat-num"></h4>
                  <div class="subtext">
                    <i class="glyphicon glyphicon-triangle-top txt-ontrack"></i>
                    Playbooks execution can extend beyond the affected asset,
                    collecting additional artifacts.
                  </div>
                </div>
              </li>
              <li class="col-md-3">
                <div class="stat-card">
                  <div class="stat-icon right">
                    <span class="bg-measure users_single-02"></span
                    ><i class="glyphicon glyphicon-home"></i>
                  </div>
                  <h2 style="font-weight: bold">User Notifications.</h2>
                  <h4 class="stat-num"></h4>
                  <div class="subtext">
                    <i class="glyphicon glyphicon-triangle-top txt-ontrack"></i>
                    Different communication channels available as part of the
                    orchestrated response.
                  </div>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div style="padding-top: 100px" class="d-grid gap-3">
        <div id="app">
          <button
            @click="toggle1 = !toggle1"
            type="button"
            class="btn btn-secondary btn-lg btn-block block"
          >
            Plugins and Integrations.
          </button>
          <div v-if="toggle1">
            <img class="show" height="250" src="img/soar1.png" alt="" />
          </div>
        </div>
        <div>
          <button
            @click="toggle2 = !toggle2"
            type="button"
            class="btn btn-secondary btn-lg btn-block block"
          >
            Workflows.
          </button>
          <div v-show="toggle2">
            <img class="show" src="img/soar2.png" alt="" />
          </div>
        </div>
        <div>
          <button
            @click="toggle3 = !toggle3"
            type="button"
            class="btn btn-secondary btn-lg btn-block block"
          >
            Apps Ecosystem.
          </button>
          <div v-show="toggle3">
            <img class="show" height="250" src="img/soar3.png" alt="" />
          </div>
        </div>
      </div>
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
</script>
<style lang="scss" scoped>
.show {
  width: 75%;
  height: 450px;
  background-repeat: no-repeat;
  background-size: contain;
  margin-left: 12%;
  margin-bottom: 50px;
}
.block {
  margin-left: 12%;
  display: block;margin-bottom: 20px;;
  width: 75%;
  justify-content: center;
  border: none;
  background-color: #0446aa;
  padding: 14px 28px;
  font-size: 16px;
  cursor: pointer;
  text-align: center;
}
ul {
  list-style-type: none;
}
h2.headings {
  margin-bottom: 20px;
}
.stat-card h3 {
  font-size: 16px;
  margin-top: 5px;
  line-height: 20px;
  padding-right: 45px;
  color: #333;
  text-align: left;
}
.stat-card {
  position: relative;
  display: inline-block;
  background-color: #fff;
  width: 320px;
  min-height: 170px;
  text-align: left;
  padding: 15px;
  border-width: 1px;
  border-style: solid;
  border-color: rgb(204, 204, 204);
  border-image: initial;
  overflow: hidden;
}
.stat-icon {
  position: absolute;
  top: 0px;
  right: 0px;
  width: 60px;
  height: 60px;
  line-height: 60px;
  text-align: center;
}
.stat-icon.right {
  right: 0px;
}
.stat-icon span {
  position: absolute;
  z-index: 8;
  top: -40px;
  left: 5px;
  width: 100px;
  height: 100px;
  line-height: 120px;
  border-radius: 50%;
}
.stat-icon i {
  padding-left: 15px;
  color: rgb(255, 255, 255);
  z-index: 9;
  font-size: 24px;
}
.bg-target {
  background-color: #e07000;
}
.txt-target {
  color: #e07000;
}
.bg-ontrack {
  background-color: #007613;
}
.txt-ontrack {
  color: #007613;
}
.bg-failing {
  background-color: #d43e3a;
}
.txt-failing {
  color: #d43e3a;
}
.bg-measure {
  background-color: #186ea5;
}
.txt-measure {
  color: #186ea5;
}
.stat-card h4.stat-num {
  font-size: 45px;
  text-align: left;
}
.stat-card .subtext {
  font-size: 15px;
}
.stat-card .source {
  font-size: 12px;
  margin-top: 15px;
}
.stat-card .open-btn {
  margin-top: 15px;
}
.typerclass {
  margin-bottom: 0px;
  font-weight: bold;
}
// all css for type writer
.img {
  width: 150px;
}
.typer {
  width: 100%;
  font-size: 3rem;
  // font-weight: bold;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
h1 {
  margin-bottom: 0px;
  font-size: 15rem;
  font-weight: normal;
  span.typed-text {
    color: #d2b94b;
    // font-size: 60px;
  }
}

// Cursor blinking CSS Starts...
.blinking-cursor {
  font-size: 3rem;
  color: #2c3e50;
  -webkit-animation: 1s blink step-end infinite;
  -moz-animation: 1s blink step-end infinite;
  -ms-animation: 1s blink step-end infinite;
  -o-animation: 1s blink step-end infinite;
  animation: 1s blink step-end infinite;
}
@keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: #2c3e50;
  }
}
@-moz-keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: #2c3e50;
  }
}
@-webkit-keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: #2c3e50;
  }
}
@-ms-keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: #2c3e50;
  }
}
@-o-keyframes blink {
  from,
  to {
    color: transparent;
  }
  50% {
    color: #2c3e50;
  }
}
// Cursor blinking CSS Ends...
</style>
