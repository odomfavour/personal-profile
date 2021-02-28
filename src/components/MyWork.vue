<template>
  <section id="work" class="section dark-bg">
    <div class="container">
      <h3 class="font-weight-bold text-uppercase my-4 text-center">{{work.name}}</h3>
      <b-row>
        <b-col md="4">
          <img
              :src="require('../assets/img/' + work.img)"
              title=""
              alt=""
              class="img-fluid"
            />
            <h5>{{work.brief}}</h5>
        </b-col>
        <b-col md="8">
          <p>{{work.note}}</p>
          <p>{{work.note1}}</p>
        </b-col>
      </b-row>
     <!-- <p> {{router}}</p> -->
      <!-- <div class="portfolio-box-01">
                <div class="portfolio-info">
                  <h5 class="white-color font-weight-bold">{{ work.name }}</h5>
                  <span>{{ work.brief }}</span>
                </div>
                <div class="portfolio-img">
                  <img
                    :src="require('../assets/img/' + work.img)"
                    title=""
                    alt=""
                    class="img-fluid"
                  />
                  <div class="portfolio-icon">
                    <a href="static/img/m-portfolio-9.jpg" class="gallery-link">
                      <span class="ti-plus"></span>
                    </a>
                  </div>
                </div>
              </div> -->
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      isWeb: true,
      isNovel: true,
      works: [
        {state: 'isWeb', name: 'Fifa-fans', link: 'hshds', img: 'about-me.c67821fd.jpg', brief: 'a web app for football fans'},
        {state: 'isNovel', name: 'More than a turn', link: 'hshds', img: 'mee.d59e77a5.jpg', brief: 'Young adult novel'},
        {state: 'isWeb', name: 'Unsplash api search', link: 'hshds', img: 'about-me.c67821fd.jpg', brief: 'a web app for football fans'},
        {state: 'isNovel', name: 'Ears that dont listen', link: 'hshds', img: 'mee.d59e77a5.jpg', brief: 'cult in school'},
        {state: 'isNovel', name: 'Where is home', link: 'hshds', img: 'mee.d59e77a5.jpg', brief: 'South Africa Xenophobia'},
        {state: 'isWeb', name: 'Country api', link: 'hshds', img: 'about-me.c67821fd.jpg', brief: 'country based'},
        ],
        // router: this.$route.params.work.name,
        work: {}
    };
  },
  methods: {
    showAll() {
      this.isWeb = true;
      this.isNovel = true;
    },
    showNovels() {
      (this.isWeb = false), (this.isNovel = true);
    },
    showWeb() {
      this.isNovel = false;
      this.isWeb = true;
    },
    getWork() {
      this.work = JSON.parse(localStorage.getItem('work'));
      
      // this.work = this.works.find(
      //     (work) => work.name === this.router,
      //   )
    }
  },
  created() {
    this.getWork()
  }
};
</script>

<style>
/* #work {
  padding: 100px 0;
}

.work-display {
  transition: cubic-bezier(0.39, 0.58, 0.57, 1) all 0.55s;
}
.portfolio-filter-01 {
  padding-top: 15px;
  padding-bottom: 15px;
}
.filter li {
  margin-right: 15px;
  padding: 5px 0;
}
.filter li .btn {
  min-width: 80px;
} */

</style>
