<template>
  <div class="navbar">
    <div class="top-navbar-container">
      <div class="top-navbar">
        <div class="left-nav">
          Home
        </div>
        <div class="right-nav">
          <div>
            About
          </div>
          <div>
            Work
          </div>
          <div>
            Blog
          </div>
          <div>
            Contact
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "baseheader",
  data() {
    return {
      burgerToggle: false,
    };
  },
};
</script>
<style scoped>
.navbar {
  position: relative;
}
.top-navbar-container {
  width: 100%;
  display: flex;
  justify-content: center;
}
.top-navbar {
  background-color: #fafafa;
  max-width: 1400px;
  width: 100%;
  display: flex;
  padding: 20px;
  justify-content: space-between;
}
.top-navbar .right-nav {
  line-height: 50px;
  width: 40%;
  display: flex;
  justify-content: space-around;
}
.nav-links {
  vertical-align: middle;
  font-weight: bold;
  color: black;
}
.bottom {
  display: none;
}

@media only screen and (max-width: 480px) {
  .top-navbar {
    display: none;
  }

  .bottom {
    display: block;
    position: fixed;
    bottom: 0;
    width: 100%;
  }
  .overlay {
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.7);
    display: flex;
    align-items: flex-end;
    justify-content: flex-end;
  }
  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 0.5s;
  }
  .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
    opacity: 0;
  }
  .bottom-nav-links {
    font-size: 30px;
    color: white;
    margin: 10px 0px 10px 0px;
  }
  .bottom-links {
    display: block;
    text-align: end;
    margin: 0px 15px 15px 0px;
  }
  .bottom-navbar {
    box-shadow: 0px -5px 30px rgba(0, 0, 0, 0.1);
    background-color: #fafafa;

    display: flex;
    justify-content: space-between;
    padding: 10px;
  }
  .bottom-navbar .left-nav {
    display: flex;
    line-height: 40px;
  }
  .bottom-navbar .right-nav {
    display: flex;
    line-height: 40px;
  }
  .bottom-navbar .name {
    padding-left: 10px;
    vertical-align: middle;
    font-weight: bold;
  }
  .bottom-navbar .name,
  .cat-img-contain {
    line-height: 55px;
  }
  .bottom-navbar .cat-img {
    height: 40px;
    vertical-align: middle;
  }
  .burger-menu {
    margin-top: 10px;
    height: 31px;
    width: 35px;
    vertical-align: middle;
  }
  .burger-menu:hover {
    cursor: pointer;
  }
  .burger {
    height: 5px;
    width: 100%;
    background: black;
    border-radius: 15px;
    margin: 4px 0px 4px 0px;
  }
}
</style>
