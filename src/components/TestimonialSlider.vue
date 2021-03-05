<template>
  <div class="container">
      <carousel-3d :autoplay="true" :autoplay-timeout="5000" :display="5" width="450">
    <slide v-for="(slide, i) in slides" :index="i" :key="i">
        <div class="p-md-4 p-3">
            <div class="row">
            <div class="col-md-5">
<div class="client-info ">
    <div>
        <div class="image-box text-center">
                <img src="../assets/img/meee.jpeg" alt="client-image" class="img-fluid">
            </div>
            <div class="name text-center">
                <h4>{{slide.name}}</h4>
            </div>
    </div>
            
          </div>
            </div>
            <div class="col-md-7">
                <div class="testimony mt-md-5">
              <p> {{slide.testimony}}.</p>
          </div>
            </div>
        </div>
        </div>
      </slide>
  </carousel-3d>
  </div>
</template>

<script>
export default {
    data() {
        return {
            slides: [
                {name: 'Ayo Ola', testimony: "Ian has done a fantastic job overall. Not only the site is to design, the code is very clean and slick." },
                {name: 'Chisom', testimony: "He has a patient spirit and is always willing to help. He's infact an Agba dev"},
                {name: 'Chilo', testimony: "Ogo writes well. His stories keep you glued and expectant for evry scene. He is also a goo developer"},
                {name: 'Nneoma Obasi', testimony: "He has a thing for novels and he just keeps you on your toes with his writing"},
                {name: 'Kelechi', testimony: "He takes web development to another level. I was shocked to see what he did with just vanilla html and css"},
                {name: 'Mrs. Treasure', testimony: "Mr. Ogochukwu teaches well, students love the way he teaches and are eager to learn too."},
                {name: 'Promise Orung', testimony: "If one is to take up a challenge, Ogochulwu is one. He has grown over time and so quickly in web development"}
                ]
        }
    }
}
</script>

<style>

    /* .image-box {
        height: 18px;
        width: 180px
    } */

    .client-info {
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .image-box img {
        border-radius: 50%;
        
    }

    @media(max-width: 900px) {
        .carousel-3d-slide.current{
            max-height: 300px !important;
        }

        .carousel-3d-slider {
             height: 300px !important;
        }

        .client-talk {
            flex-direction: column;
        }
        .image-box {
        height: 70px;
        width: 70px;
        text-align: center;
    }
    }
</style>