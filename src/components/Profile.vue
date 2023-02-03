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
        <div class="profilepic clr-white">
          <div class="flex-div">
            <img src="images/Anne.png" />
          </div>
          <p class="profilename flex-div-">@Anne</p>
        </div>
      </div>
      <br />
      <div class="container">
        <div class="vid-list clr-white">
          <a href=""><img src="images/img3.jpg" class="thumbnail" /></a>
          <div class="flex-div">
            <img src="images/Anne.png" />
            <div class="vid-info">
              <a href="">@username </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { useRouter } from "vue-router";

const router = useRouter();
// const route = useRoute();

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
.flex-div- {
  background-color: #ffffff;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 3%;
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
  background-color: #fff;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  grid-column-gap: 16px;
  grid-row-gap: 30px;
  margin-top: 15px;
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
.profilename p {
  background-color: #fff;
  margin: auto;
  justify-content: center;
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

@media (max-width: 900px) {
  .sidebar {
    display: none;
  }
  .container,
  .large-container {
    padding-left: 5%;
    padding-right: 5%;
  }
  .nav-right img {
    display: none;
  }
  .nav-right .user-icon {
    display: block;
    width: 30px;
  }
  .nav-middle .search-box input {
    width: 100px;
  }
  .nav-middle .mic-icon {
    display: none;
  }
  .logo {
    width: 90px;
  }
}

/*------------------play video page------------------*/
.play-container {
  padding-left: 2%;
}
.row {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
.play-video {
  flex-basis: 69%;
}
.right-sidebar {
  flex-basis: 30%;
}
.play-video video {
  width: 100%;
}

.side-video-list {
  display: flex;
  justify-content: space-between;
  margin-bottom: 8px;
}
.side-video-list img {
  width: 100%;
}
.side-video-list .small-thumbnail {
  flex-basis: 49%;
}
.side-video-list .vid-info {
  flex-basis: 49%;
}
.play-video .tags a {
  color: #0000ff;
  font-size: 13px;
}
.play-video h3 {
  font-weight: 600;
  font-size: 22px;
}
.play-video .play-video-info {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  margin-top: 10px;
  font-size: 14px;
  color: #5a5a5a;
}
.play-video .play-video-info a img {
  width: 20px;
  margin-right: 8px;
}
.play-video .play-video-info a {
  display: inline-flex;
  align-items: center;
  margin-left: 15px;
}
.play-video hr {
  border: 0;
  height: 1px;
  background: #ccc;
  margin: 10px 0;
}
.publisher {
  display: flex;
  align-items: center;
  margin-top: 20px;
}
.publisher div {
  flex: 1;
  line-height: 18px;
}
.publisher img {
  width: 40px;
  border-radius: 50%;
  margin-right: 15px;
}
.publisher div p {
  color: #000;
  font-weight: 600;
  font-size: 18px;
}
.publisher div span {
  font-size: 13px;
  color: #5a5a5a;
}
.publisher button {
  background: red;
  color: #fff;
  padding: 8px 30px;
  border: 0;
  outline: 0;
  border-radius: 4px;
  cursor: pointer;
}
.vid-description {
  padding-left: 55px;
  margin: 15px 0;
}
.vid-description p {
  font-size: 14px;
  margin-bottom: 5px;
  color: #5a5a5a;
}
.vid-description h4 {
  font-size: 14px;
  color: #5a5a5a;
  margin-top: 15px;
}
.add-comment {
  display: flex;
  align-items: center;
  margin: 30px 0;
}
.add-comment img {
  width: 35px;
  border-radius: 50%;
  margin-right: 15px;
}
.add-comment input {
  border: 0;
  outline: 0;
  border-bottom: 1px solid #ccc;
  width: 100%;
  padding-top: 10px;
  background: transparent;
}
.old-comment {
  display: flex;
  align-items: center;
  margin: 20px 0;
}
.old-comment img {
  width: 35px;
  border-radius: 50%;
  margin-right: 15px;
}
.old-comment h3 {
  font-size: 14px;
  margin-bottom: 2px;
}
.old-comment h3 span {
  font-size: 12px;
  color: #5a5a5a;
  font-weight: 500;
  margin-left: 8px;
}
.old-comment .comment-action {
  display: flex;
  align-items: center;
  margin: 8px 0;
  font-size: 14px;
}
.old-comment .comment-action img {
  border-radius: 0;
  width: 20px;
  margin-right: 5px;
}
.old-comment .comment-action span {
  margin-right: 20px;
  color: #5a5a5a;
}
.old-comment .comment-action a {
  color: #0000ff;
}

@media (max-width: 900px) {
  .play-video {
    flex-basis: 100%;
  }
  .right-sidebar {
    flex-basis: 100%;
  }
  .play-container {
    padding-left: 5%;
  }
  .vid-description {
    padding-left: 0;
  }
  .play-video .play-video-info a {
    margin-left: 0;
    margin-right: 15px;
    margin-top: 15px;
  }
}
</style>
