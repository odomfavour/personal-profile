<template>
  <div id="app" >
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/work">Work</router-link>
    </div> -->
    <router-view/>
  </div>
</template>
<script>
export default {
  
}
</script>

<style>
@font-face {
    font-family: rubik;
    src: url(/fonts/Rubik/static/Rubik-Regular.ttf) !important;
}
body {
    font-family: rubik !important;
}

@media(max-width: 900px) {
        .side-bar {
            z-index: 6666777;
        }
    }
</style>
