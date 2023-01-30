<template>
  <section class="indent-1">
    <section class="section"></section>
    <!-- component side -->
    <section>
      <div id="myID" class="bottomMenu">
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
  </section>
</template>

<script>
export default {
  name: "RightSidePopUps",
  props: {
    msg: String,
  },
  mounted() {
    myID = document.getElementById("myID");
    var userM = document.getElementById("user");
    var secM = document.getElementById("secondDellMsg");
    var myScrollFunc = function () {
      var y = window.scrollY;
      // if (y < 1200) {
      //   myID.className = "bottomMenu hide";
      // }
      // if (y > 1800) {
      //   myID.className = "bottomMenu show";
      // }
      // if (y > 2700) {
      //   myID.className = "bottomMenu show large";
      // }
      if (y < 11546) {
        myID.className = "bottomMenu hide";
        userM.className = "userMessage hide";
        secM.className = "secondDellMenu hide";
      }
      if (y < 11550) {
        myID.className = "bottomMenu show";
        userM.className = "userMessage show";
        secM.className = "secondDellMenu show";
      }
      if (y > 4500) {
        myID.className = "bottomMenu hide";
        userM.className = "userMessage hide";
        secM.className = "secondDellMenu hide";
      }
      console.log(y);
    };

    window.addEventListener("scroll", myScrollFunc);
  },
};
</script>

<style>
.bottomMenu {
  position: fixed;
  width: 300px;
  height: 51px;
  z-index: 1;
  transition: 0.5s;
  box-shadow: 0 4px 10px rgb(0 0 0 / 8%);
  background: #003862;
  color: white;
  top: 98px;
  right: 205px;
  padding: 40px;
}
.message-text {
  position: relative;
  text-align: left;
  bottom: 150px;
  font-family: Roboto;
  font-size: 22px;
  width: 315px;
}
.userMessage {
  position: fixed;
  width: 300px;
  height: 100px;
  z-index: 1;
  transition: 2.5s;
  box-shadow: 0 4px 10px rgb(0 0 0 / 8%);
  background: #0970c8;
  color: white;
  top: 294px;
  right: 106px;
  padding: 39px;
}

.userMessage-text {
  position: relative;
  text-align: left;
  bottom: 150px;
  font-family: Roboto;
  font-size: 22px;
  padding: 10px;
}

.secondDellMenu {
  position: fixed;
  width: 300px;
  height: 51px;
  z-index: 1;
  transition: 3s;
  box-shadow: 0 4px 10px rgb(0 0 0 / 8%);
  background: #003862;
  color: white;
  bottom: 179px;
  right: 205px;
  padding: 40px;
}
.indent-1 {
  float: left;
}
.indent-1 section {
  width: 50%;
  float: left;
}
.hide {
  opacity: 0;
}
.show {
  opacity: 0.85;
}
</style>
