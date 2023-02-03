<template>
  <div class="background" :class="{ otherColor: isSignIn }">
    <div id="app">
      <nav class="flex-div">
        <div class="nav-left flex-div">
          <h1>
            <a><span class="menu icon">You More</span></a>
          </h1>
        </div>
        <div class="nav-middle flex-div nav-bg">
          <div class="search-box flex-div">
            <input type="text" placeholder="Search" />
            <img src="images/search.png" />
          </div>
        </div>
        <div class="nav-right flex-div nav-bg">
          <a class="nav-bg" href="/settings"> <img src="images/more.png" /> </a>
          <a class="nav-bg" href="/profile"
            ><img src="images/Anne.png" class="user-icon"
          /></a>
        </div>
      </nav>

      <!----------------sidebar--------------->

      <div class="sidebar">
        <div class="shortcut-links">
          <a href="/home">
            <img src="images/home.png" />
            <p>Home</p></a
          >
          <a href="">
            <img src="images/explore.png" />
            <p>Favorites</p></a
          >
          <a href="">
            <img src="images/upload.png" />
            <p>Create Post</p></a
          >
          <hr />
        </div>
      </div>

      <!----------------main--------------->
      <br />
      <div class="container">
        <a>
          <div class="list-container">
            <p class="center">Change Email</p>
          </div>
        </a>
        <a>
          <div class="list-container">
            <p class="center">Change Username</p>
          </div>
        </a>
        <a>
          <div class="list-container">
            <p class="center">Change Password</p>
          </div>
        </a>
      </div>
      <div class="container-new">
        <div class="container-">
          <RouterLink to="/" style="background: #f4bb44" class="logout">
            logout
          </RouterLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { useRouter } from "vue-router";

const router = useRouter();
// const route = useRoute();

const goToLoginPage = () => {
  router.push({ name: "login" });
};

export default {
  computed: {
    isSignIn() {
      return this.$route.path === "/signIn";
    },
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  font-family: "poppins", sans-serif;
  box-sizing: border-box;
  background-color: #f5f5dc;
}
.center {
  background: #ffffff;
  margin: auto;
  width: 58%;
}
.background {
  height: 100vh;
  width: 100vw;
  background-color: #f5f5dc;
}

.otherColor {
  background-color: #f5f5dc;
}

a {
  text-decoration: unset;
  color: #5a5a5a;
}
img {
  cursor: pointer;
}
.flex-div {
  display: flex;
  align-items: center;
}
nav {
  padding: 10px 2%;
  justify-content: space-between;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  background: #fff;
  position: sticky;
  top: 0;
  z-index: 10;
}
.nav-bg {
  background: #fff;
}
.nav-right img {
  background: #fff;
  width: 25px;
  margin-right: 25px;
}
.nav-right .user-icon {
  width: 35px;
  border-radius: 50%;
  margin-right: 0;
}
.nav-left .menu-icon {
  background: #fff;
  width: 22px;
  margin-right: 25px;
  font-size: 56px;
  font-weight: 300;
  font-style: normal;
}
.nav-left .logo {
  background: #fff;
  width: 130px;
}
.nav-middle .mic-icon {
  background: #fff;
  width: 16px;
}
.nav-middle .search-box {
  background: #fff;
  border: 1px solid #ccc;
  margin-right: 15px;
  padding: 8px 12px;
  border-radius: 25px;
}
.nav-middle .search-box input {
  background: #fff;
  width: 400px;
  border: 0;
  outline: 0;
  background: transparent;
}
.nav-middle .search-box img {
  background: #fff;
  width: 15px;
}

/* --------------sidebar------------*/

.sidebar {
  background: #f5f5dc;
  width: 15%;
  height: 100vh;
  position: fixed;
  top: 0;
  padding-left: 2%;
  padding-top: 80px;
}
.shortcut-links a img {
  width: 20px;
  margin-right: 20px;
}
.shortcut-links a {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
  width: fit-content;
  flex-wrap: wrap;
}
.shortcut-links a:first-child {
  color: #ed3833;
}
.sidebar hr {
  border: 0;
  height: 1px;
  background: #ccc;
  width: 85%;
}

.small-sidebar {
  width: 5%;
}
.small-sidebar a p {
  display: none;
}
.small-sidebar h3 {
  display: none;
}
.small-sidebar hr {
  width: 50%;
  margin-bottom: 25px;
}

/*----------- main ----------*/
.container {
  margin: auto;
  background: #ffffff;
  width: 500px;
  padding: 50px;
  padding-top: 3%;
  border-radius: 10px;
}
.container-new {
  margin: auto;
  width: 500px;
  padding: 10px;
  padding-top: 3%;
  border-radius: 10px;
}
.container- .logout {
  margin: auto;
  font-size: 16px;
  line-height: 28px;
  padding: 8px 16px;
  width: 30%;
  min-height: 44px;
  border: unset;
  border-radius: 4px;
  outline-color: rgb(84 105 212 / 0.5);
  background-color: rgb(255, 255, 255);
  box-shadow: rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgba(0, 0, 0, 0) 0px 0px 0px 0px,
    rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgba(60, 66, 87, 0.16) 0px 0px 0px 1px,
    rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgba(0, 0, 0, 0) 0px 0px 0px 0px,
    rgba(0, 0, 0, 0) 0px 0px 0px 0px;
}

.logout {
  background-color: rgb(84, 105, 212);
  box-shadow: rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgba(0, 0, 0, 0) 0px 0px 0px 0px,
    rgba(0, 0, 0, 0.12) 0px 1px 1px 0px, rgb(84, 105, 212) 0px 0px 0px 1px,
    rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgba(0, 0, 0, 0) 0px 0px 0px 0px,
    rgba(60, 66, 87, 0.08) 0px 2px 5px 0px;
  color: #fff;
  font-weight: 600;
  cursor: pointer;
}
.large-container {
  padding-left: 7%;
}
.banner {
  width: 100%;
}
.banner img {
  width: 100%;
  border-radius: 8px;
}
.list-container {
  background: fixed;
  margin: auto;
  width: 400px;
  padding: 25px;
}
.vid-list .thumbnail {
  background-color: #fff;
  width: 100%;
  border-radius: 5px;
}
.vid-list .flex-div {
  background-color: #fff;
  align-items: flex-start;
  margin-top: 7px;
}
.profilepic .flex-div {
  background-color: #fff;
  margin: auto;
}
.profilepic .flex-div img {
  background-color: #fff;
  border-radius: 50%;
  margin: auto;
}
.profilename .flex-div {
  background-color: #fff;
  justify-content: center;
  align-items: center;
}
.profilename p {
  background-color: #fff;
  margin: auto;
}
.vid-list .flex-div img {
  background-color: #fff;
  width: 35px;
  margin-right: 10px;
  border-radius: 50%;
}
.vid-info {
  background-color: #fff;
  color: #5a5a5a;
  font-size: 13px;
}
.vid-info a {
  background-color: #fff;
  color: #000;
  font-weight: 600;
  display: block;
  margin-bottom: 5px;
}
.clr-white {
  background-color: #fff;
}
</style>
