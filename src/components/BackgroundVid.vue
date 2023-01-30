<template>
  <section>
    <div id="setHeight"></div>
    <video
      :key="video"
      id="v0"
      tabindex="0"
      autobuffer="autobuffer"
      preload="preload"
      autoplay
      loop
      muted
    >
      <source
        type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"'
        src="../assets/officetodesk.mp4"
      />
    </video>
  </section>
  <div id="topLeft">
    <img src="../assets/DellComponentsLogo.png" alt="" />
  </div>
  <div id="topRight">
    <img src="../assets/RightCorner.png" alt="" />
  </div>

  <!-- <section class="section">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="content">
            <p>
              Back in January, Nicole attended CES, where she was able to
              explore the Dell booth.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="section">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="content">
            <p>
              Dell hosted an interactive experience that showed how integrated
              hardware management and machine learning can help healthcare
              professionals track and measure treatment efficacy across hospital
              systems.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section> -->

  <!-- <section class="indent-1">
    <section class="section">
      <div class="container">
        <div class="row">
          <div class="col-12">
            <div class="content">
              <p>
                After Nicole talks with a Dell representative about her goals,
                concerns and needs, the representative suggests Dell&apos;s
                white-glove service.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section> -->
  <!-- component side -->
  <!-- <section>
      <div id="myID" class="bottomMenu hide">
        <img
          style="right: 208px; bottom: 55px; position: relative"
          src="../assets/FirstMessage.png"
        />
        <img
          style="position: relative; bottom: 34px; right: 315px"
          src="../assets/Dell-Rep.png"
        />
        <div class="message-text">
          Hi! Welcome to Dell&apos;s Services for Enterprise. What can we do for
          you?
        </div>
      </div>
      <div id="user" class="userMessage hide" style="align-items: flex-end">
        <h5
          style="
            position: relative;
            text-align: right;
            font-family: Roboto;
            font-size: 25px;
            bottom: 111px;
            font-weight: 350;
            left: 40px;
          "
        >
          Nicole
        </h5>
        <div class="userMessage-text">
          I am a Service Desk Director in a hospital system and we are looking
          into providers for end user hardware systems to upgrade our machines.
        </div>
      </div>
      <div id="secondDellMsg" class="secondDellMenu hide">
        <img
          style="right: 208px; bottom: 55px; position: relative"
          src="../assets/FirstMessage.png"
        />
        <img
          style="position: relative; bottom: 34px; right: 315px"
          src="../assets/Dell-Rep.png"
        />
        <div class="message-text">
          We can absolutely help with that! Our white-glove service would be
          perfect for your needs.
        </div>
      </div>
    </section>
  </section> -->
  <!-- End of components -->
  <!-- <section class="section">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="content">
            <p>
              This service will help gain alignment among stakeholders across
              departments at the hospital.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section> -->
</template>

<script>
export default {
  name: "BackgroundVid",
  props: {
    msg: String,
  },
  // mounted() {
  //   var frameNumber = 0, // start video at frame 0
  //     // lower numbers = faster playback
  //     playbackConst = 500,
  //     // get page height from video duration
  //     setHeight = document.getElementById("set-height"),
  //     // select video element
  //     vid = document.getElementById("v0");
  //   // var vid = $('#v0')[0]; // jquery option

  //   // dynamically set the page height according to video length
  //   vid.addEventListener("loadedmetadata", function () {
  //     setHeight.style.height = Math.floor(vid.duration) * playbackConst + "px";
  //   });

  //   // Use requestAnimationFrame for smooth playback
  //   function scrollPlay() {
  //     var frameNumber = window.pageYOffset / playbackConst;
  //     vid.currentTime = frameNumber;
  //     window.requestAnimationFrame(scrollPlay);
  //     // console.log("frame number: ", frameNumber);
  //   }

  //   window.requestAnimationFrame(scrollPlay);

  //   function hidePortal() {
  //     var x = document.getElementById("portal");
  //     if (x.style.display === "none") {
  //       x.style.display = "block";
  //     } else {
  //       x.style.display = "none";
  //     }
  //   }
  // },
};
</script>

<style scoped>
body {
  background-color: #c6d7de;
  font-family: "Montserrat";
  padding: 3em;
  /* height: 100vh; */
}

#v0 {
  position: fixed;
  bottom: 0;
  right: 0;
  width: 100%;
}

#set-height {
  display: block;
}

section {
  z-index: 1;
  position: relative;
}

.content {
  position: sticky;
  position: -webkit-sticky;
  /* top: 33.3%; */
  font-family: Roboto;
  font-size: 35px;
  text-align: left;
  color: white;
  width: 700px;
  padding: 45px;
  margin: 60px;
}

h1 {
  font-size: 3em;
  background: #fff;
  display: inline-block;
  padding: 10px 15px;
  border-radius: 5px;
  margin: 0;
}
.indent-1 {
  float: left;
}
.indent-1 section {
  width: 50%;
  float: left;
}

p {
  font-size: 1.5em;
}

section:nth-of-type(1) {
  height: 1200px;
}
section:nth-of-type(2) {
  height: 1200px;
}
section:nth-of-type(3) {
  height: 1200px;
}
section:nth-of-type(4) {
  height: 1000px;
}
section:nth-of-type(5) {
  height: 4000px;
}

.entered {
  -webkit-animation: text-focus-in 1s cubic-bezier(0.55, 0.085, 0.68, 0.53) both;
  animation: text-focus-in 1s cubic-bezier(0.55, 0.085, 0.68, 0.53) both;
}

#portal {
  /* background-image: url('/men_sc001_sh005.1001.png'); */
  height: 100vh;
  width: 100vw;
  bottom: 60px;
  right: 60px;
}
#topLeft {
  position: relative;
}
#topLeft img {
  top: 33px;
  left: 42px;
  position: fixed;
  z-index: 2;
}
#topRight {
  position: relative;
}
#topRight img {
  top: 66px;
  right: 46px;
  position: fixed;
  z-index: 2;
}
/* ----------------------------------------------
 * Generated by Animista on 2018-7-4 16:24:12
 * w: http://animista.net, t: @cssanimista
 * ---------------------------------------------- */

/**
 * ----------------------------------------
 * animation text-focus-in
 * ----------------------------------------
 */
@-webkit-keyframes text-focus-in {
  0% {
    -webkit-filter: blur(12px);
    filter: blur(12px);
    opacity: 0;
  }
  100% {
    -webkit-filter: blur(0px);
    filter: blur(0px);
    opacity: 1;
  }
}
@keyframes text-focus-in {
  0% {
    -webkit-filter: blur(12px);
    filter: blur(12px);
    opacity: 0;
  }
  100% {
    -webkit-filter: blur(0px);
    filter: blur(0px);
    opacity: 1;
  }
}
</style>
