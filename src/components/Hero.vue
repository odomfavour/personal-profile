<template>
  <div id="hero-section">
    <div class="container">
      <div class="d-flex justify-content-between py-4 px-2">
        <div class="info">
          <label class="mr-3">+234 806-7488-682</label>
          <label>ogochukwuodom@gmail.com</label>
        </div>
        <div class="lang">
          <div v-on:click="openMobileNav()" id="burger">
            <div class="line1"></div>
            <div class="line2"></div>
            <div class="line3"></div>
          </div>
        </div>
      </div>
      <div class="row full-screen align-items-center">
        <div class="col-md-7 order-md-1 order-2">
          <div class="type-box mt-md-3 mt-5">
            <h6>Hello, My name is</h6>
            <h1 class="dev-name">Ogochukwu Odom</h1>
            <h4 class="lead">Front-end Developer | Writer | Tutor</h4>
            <p class="desc">
              I develop services for customers of all sizes, specializing in
              creating stylish, modern websites, web services and online stores.
            </p>
            <div class="btn-bar">
              <button class="btn btn-warning download">Download CV</button>
            </div>
          </div>
        </div>
        <div class="col-md-5 order-md-2 order-1">
          <img src="../assets/img/its-mee.png" alt="" class="img-fluid" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  props: ["name", "logoImg", "navLinks"],
  methods: {
    openMobileNav() {
      const burger = document.getElementById("burger");
      const nav = document.querySelector(".side-bar");
      console.log(nav);
      // const navLinks = document.querySelectorAll('.nav-links li')
      // Toggle navigation on mobile
      nav.classList.toggle("nav-active");
      // Burger toggler
      burger.classList.toggle("toggle");
      // Animate navigation links
      //     navLinks.forEach((link, index) => {
      //         if (link.style.animation || link.style.webkitAnimation) {
      //             link.style.animation = ''
      //             link.style.webkitAnimation = ''
      //         } else {
      //             link.style.webkitAnimation = `navLinkFade 0.5s ease forwards ${
      //             index / 7
      //         }s`
      //             link.style.animation = `navLinkFade 0.5s ease forwards ${index / 7}s`
      //         }
      //     })
      // }
    },
  },
};
</script>

<style scoped>
#hero-section {
  min-height: 100vh;
}

.type-box h6{
  font-size: 20px;
  font-weight: 500;
  margin: 0 0 20px;
}

.dev-name {
  font-size: 70px;
  font-weight: 700;
  line-height: 1;
  margin: 0 0 20px;
}

.lead {
  text-transform: uppercase;
}



#burger {
  display: none;
  cursor: pointer;
}

#burger div {
  width: 30px;
  height: 3px;
  margin: 8px;
  background-color: #fefefe;
  transition: all 0.3s ease-in;
}

.toggle .line1 {
  transform: rotate(-45deg) translate(-9px, 10px);
}

.toggle .line2 {
  opacity: 0;
}

.toggle .line3 {
  transform: rotate(45deg) translate(-5px, -6px);
}

.btn:hover::before {
  opacity: 1;
  filter: alpha(opacity=100);
  -webkit-transform: translateX(0);
  transform: translateX(0);
}

.download:hover::before {
  font: 15px/1.2em FontAwesome;
  color: #fff;
  position: absolute;
  height: 100%;
  right: 25px;
  top: 50%;
  margin-top: -9px;
  transition: all 0.3s;
  opacity: 0;
  /* filter: alpha(opacity=0);
    -webkit-transform: translateX(-20px); */
  transform: translateX(-20px);
}

@media (max-width: 900px) {
  .dev-name {
    font-size: 40px;
  }

  #burger {
    display: block;
  }

  .side-bar {
    z-index: 6666777;
  }

  .lang {
    position: fixed;
    top: 13px;
    right: 9px;
    z-index: 9999;
    background: linear-gradient(45deg, #969ea0 10%, #5e767b 40%);
  }

  .nav-active {
    transform: translateX(40px) !important;
  }
}
</style>
