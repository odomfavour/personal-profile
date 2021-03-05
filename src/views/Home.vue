<template>
  <div class="home" >
    <SideBar />
    <main data-spy="scroll" data-target="#navbar-example2" data-offset="0">
      <Hero/>
      <Bio/>
      <TestimonialSlider/>
      <Experience/>
      <Work/>
      <Contact/>
      <Footer/>
    </main>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import SideBar from "@/components/SideBar.vue";
import Bio from "@/components/Bio.vue";
import Hero from "@/components/Hero.vue";
import TestimonialSlider from "@/components/TestimonialSlider.vue";
import Experience from "@/components/Experience.vue";
import Work from "@/components/Work.vue";
import Contact from "@/components/Contact.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    // HelloWorld,
    SideBar,
    Bio,
    Hero,
    Experience,
    TestimonialSlider,
    Work,
    Contact,
    Footer
  },
  
};
</script>

<style>
main {
  padding-left: 80px;
  background-image: linear-gradient(45deg, #969ea0 10%, #5e767b 40%, #b9c3c4);
  color: #fff;
}

@media (max-width: 700px) {
  .side-bar {
    max-height: 400px;
    overflow-x: hidden;
    overflow-y: scroll;
    display: none;
  }

  main {
    padding-left: 0;
  }
}
</style>
