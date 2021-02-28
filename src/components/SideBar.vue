<template>
  <div>
    <div class="side-bar" :class="{ active: active}" >
      <div class="hl-top">
        <div class="hl-logo text-center">
          <a href="#hero-section" class="brand">
            <b-icon icon="x-diamond-fill" font-scale="1.3"></b-icon>
          </a>
        </div>
      </div>
      <ul class="nav nav-menu py-5" id="#navbar-example2">
        <li class="w-100 text-center" v-for="(item, index) in items" :key="item.reference"  @click.stop="toggleActive(index)">
          <a class="nav-link py-3" :href="item.reference" :class="activeIndex == index? 'active': ''" :active="index === activeIndex">
            <b-icon variant="light" :icon="item.icon" font-scale="1.8"></b-icon>
          </a>
        </li>
        <!-- <li class="w-100 text-center">
          <a class="nav-link py-2" href="#about">
            <i class="fa fa-cubes"></i>
          </a>
        </li>
        <li class="w-100 text-center">
          <a class="nav-link py-2" href="#resume">
            <i class="fa fa-file"></i>
          </a>
        </li>
        <li class="w-100 text-center">
          <a class="nav-link py-2" href="#work">
            <i class="fa fa-briefcase"></i>
          </a>
        </li>
        <li class="w-100 text-center">
          <a class="nav-link py-2" href="#blog">
            <i class="fa fa-comments"></i>
          </a>
        </li>
        <li class="w-100 text-center">
          <a class="nav-link py-2" href="#contactus">
            <i class="fa fa-envelope"></i>
          </a>
        </li> -->
      </ul>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            items: [
            { reference: "#hero-section", icon: "house-fill" },
            { reference: "#about", icon: "person" },
            { reference: "#resume", icon: "file" },
            { reference: "#work", icon: "briefcase-fill" },
            { reference: "#blog", icon: "chat-dots-fill" },
            { reference: "#contactus", icon: "mailbox2" },
            
            ],
            activeIndex: 0,
            active: '',
            activeNav: false,
        }
    },
    methods: {
        toggleActive(index) {
         this.activeIndex = index;
         let sidebar = document.querySelector(".side-bar")
         let burger = document.querySelector("#burger")
         sidebar.classList.remove('nav-active');
         burger.classList.remove('toggle');
         console.log(sidebar)
         console.log(burger)
        }
    },
};
</script>

<style scoped>
.side-bar {
  width: 80px;
  position: fixed;
  display: block;
  height: 100%;
  bottom: 0;
  top: 0;
  background: #0c0c14;
  border-right: 1px solid rgba(11, 11, 19, 0.1);
}

@media (max-width: 700px) {
  .side-bar {
    max-height: 100vh;
    overflow-x: hidden;
    overflow-y: scroll;
    transition: 1.2s ease;
    transform: translateX(-100px) !important;
  }
  .nav-active {
    transform: translateX(0px) !important;
    transition: 1.2s ease;
  }
}

.brand i {
  font-size: 30px;
}

.nav-menu i {
  color: #fff;
  font-size: 25px;
  width: 40px;
  height: 40px;
  line-height: 40px;
}

.b-icon.bi:hover {
  color: #ff9301 !important;
}

li {
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.nav-menu .active .b-icon.bi{
  color: #ff9301 !important;
}

.hl-top a {
  background: #ff9301;
  color: #fff;
  font-weight: 600;
  text-decoration: none;
  font-size: 40px;
  height: 80px;
  width: 80px;
  line-height: 80px;
  display: inline-block;
  vertical-align: top;
  text-align: center;
}
</style>
