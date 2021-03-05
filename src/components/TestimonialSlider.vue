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
                <h4>John Doe</h4>
            </div>
    </div>
            
          </div>
            </div>
            <div class="col-md-7">
                <div class="testimony">
              <p> I know he will keep improving my website and advising me in the best ways forward for years to come, with SEO and new features.</p>
          </div>
            </div>
        </div>
        </div>
        
      <!-- <div class="d-flex client-talk p-4">
          
          
      </div> -->
      </slide>
  </carousel-3d>
  </div>
</template>

<script>
export default {
    data() {
        return {
            slides: 7
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