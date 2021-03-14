<template>
  <section id="work" class="section dark-bg">
    <div class="container">
      <div class="title">
        <h3>My Portfolio.</h3>
      </div>
      <div class="portfolio-filter-01">
        <ul class="filter nav">
          <li class="active" data-filter="*" @click="showAll">
            <button
              class="btn px-2"
              :class="
                isWeb === true && isNovel === true ? 'btn-warning' : 'btn-light'
              "
            >
              All
            </button>
          </li>
          <li data-filter=".branding" class="" @click="showWeb">
            <button
              class="btn px-2"
              :class="
                isWeb === true && isNovel === false
                  ? 'btn-warning'
                  : 'btn-light'
              "
            >
              Web Apps
            </button>
          </li>
          <li data-filter=".photoshop" class="" @click="showNovels">
            <button
              class="btn px-2"
              :class="
                isWeb === false && isNovel === true
                  ? 'btn-warning'
                  : 'btn-light'
              "
            >
              Novels
            </button>
          </li>
        </ul>
      </div>
      <!-- Portfolio Filter -->
      <!-- <transition-group>
                    
                </transition-group> -->
      <div class="row work-display">
        <template v-for="(work, index) in works">
          <div
            class="col-md-4 mb-3"
            :key="index"
            v-if="work.state == 'isWeb' ? isWeb : isNovel"
          >
            <!-- {{ work.state }} -->
            <!-- <router-link :to="{ name: 'Work', params: { id: work.name } }"> -->
            <div class="portfolio-box-01">
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
              <div class="portfolio-info">
                <div class="d-flex justify-content-between">
                  <div>
                    <h5 class="white-color font-weight-bold">{{ work.name }}</h5>
                    <span>{{ work.brief }}</span>
                  </div>
                  <div class="link-box" @click="showWork(work)">
                    <b-icon icon="arrow-right" variant="primary"></b-icon>
                  </div>
                </div>
                
              </div>
            </div>

            <!-- </router-link> -->
          </div>
        </template>
      </div>
      
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
        {
          state: "isWeb",
          name: "Fifa-fans",
          link: "hshds",
          img: "about-me.jpg",
          brief: "a web app for football fans",
        },
        {
          state: "isNovel",
          name: "More than a turn",
          link: "hshds",
          img: "mee.jpg",
          brief: "Young adult novel",
          note:
            "It was like screeching, the same type of sound that cars made on the race tracks. But, unlike having the screeching done by tyres of vehicles, it was rather thoughts. A thousand and one rushing through Janet's head as she sat still on the pavement in front of her house. The afternoon sun was beginning to set. For over an hour, she had been seated there staring at the distant horizon. Her head was reeling and it was as if it was going to implode the next moment. The sound of little children playing beside the house did not seem to even draw the slightest of her attention. Her mind was indeed far off, lost in her world of worry. She had tried sleeping but it was as though sleep had scurried away from her eyes. And now the images were coming again.'Thief ooo!!' It was the sound of female students jeering at her as she walked face down with her face looking down at the floor. Her school bag hung on her back as she walked in between the lines of students standing on a queue for morning assembly. She could feel the cold hands of shame cover her as too those steps. If the ground could open, she would have wished that it opened and swallowed her that very moment. Few minutes ago, the principal had just given her a suspension letter in front of everyone based on the theft that had happened in their class some weeks back. Standing among the crowd of students jeering was the real culprit -her friend Linda.For the past three weeks, Linda had not stepped even a foot in her house. Unlike in the the past, they had been best of friends. Now and again, she was always at her houses and they spent quite a while together. But after this public disgrace, as much as the grain of Sand from her shoes were never seen within the environs.'Sis, I'm going to buy fuel for the generator.' A voice said beside her. She didn't even blink an eyelid to look at whoever it was that spoke. The young boy- about fifteen years and clad in blue shirt and a black trousers stood for a while staring at her. He wondered what seemed to be bothering her. Since morning, she had been acting all weird and solemn. She even avoided eating her breakfast and just scratched her lunch.",
          note1:
            "After a while, she rose up to floor and walked off. Her butt was still smeared with the dust but that didn't even bother her. Her reputation had been dented and that was worse. It hurt deep into her soul. The ground was sandy, thus making each step she took feel like she was going to sink in. Slowly, she trudged on. One of the boys kicked the football and suddenly, there were screams. The ball had almost hit Janet on her face. Nevertheless, she did not even mind that something had almost hit her as she walked across where the boys were playing the football.The evening breeze was cool, she could feel it's chills as she continued on. Her eyes moving from left to right.  She needed someone to talk to and she was heading off to the only close friend she had -- Stanley.Darkness had soon began to claim ownership of the atmosphere. Birds chirped as well as insects but she still remained calm and solemn. Finally, after ten minutes, she arrived at a bungalow. Janet heaved a sigh before she continued to the house. She stepped on the cemented pavement leading into the house. Lying in front of the door were some footwear which she steeped on. Raising her hand, she wanted to knock on the door but noticed that it was slightly open. She wanted to speak but her heart was too heavy to let the words come out. She moved into the house walking through the narrow corridor. It was dark but she managed to walk through it using the mental picture she had of it. Then on stepping into the sitting room, her eyes nearly popped out of it's sockets.For some moments, she stood watching hands move over bodies, smooching and everything. Pain and hurt welled up in her heart as the sound of each kiss spread into the atmosphere. 'Stanley!!' She yelled aloud without even knowing when or how the words came out of her mouth. The boy and the girl who were seated on the seat there jolted at the sound of her voice. Quickly, they turned to see her standing by with her hand on her chest. Stanley rose up from the seat quickly and for some seconds, he tried to mutter things. Janet was too dazed to comprehend what he'd been saying. She was hurt, deeply hurt. She could feel the knife pierce through her heart. Turning, she raced off in the dark.  'Janet.' Stanley called as she followed her. She wouldn't listen. He wasn't worth listening to. 'Janet stop!!'The sound of his voice didn't even make her to think of stopping instead it made her intensify her strides. Her world seemed to be caving in and she couldn't make sense of anything. Running seemed to be the only thing to do now.",
        },
        {
          state: "isWeb",
          name: "Unsplash api search",
          link: "hshds",
          img: "about-me.jpg",
          brief: "Image search",
        },
        {
          state: "isNovel",
          name: "Ears that dont listen",
          link: "hshds",
          img: "mee.jpg",
          brief: "cult in school",
        },
        {
          state: "isWeb",
          name: "Country Search",
          link: "https://polydactyl-curse-fear.glitch.me/",
          img: "mee.jpg",
          brief: "Searching Countries",
        },
        {
          state: "isNovel",
          name: "Where is home",
          link: "hshds",
          img: "mee.jpg",
          brief: "South Africa Xenophobia",
        },
        {
          state: "isWeb",
          name: "Country api",
          link: "https://chartreuse-alabaster-thyme.glitch.me/",
          img: "about-me.jpg",
          brief: "country based",
        },
        {
          state: "isWeb",
          name: "huntr",
          link: "https://brave-wescoff-f58b5e.netlify.app",
          img: "about-me.jpg",
          brief: "list jobs (API) & auth (firebase)",
        },
      ],
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
    showWork(page) {
      localStorage.setItem("work", JSON.stringify(page));
      console.log(page.name);
      if(page.state == 'isNovel') {
         const workId = page.name;
      this.$router.push({ name: "Work", params: { id: workId } });
      }else {
        window.open(page.link);
      }
     
    },
  },
};
</script>

<style>
#work {
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
}

.portfolio-box-01 {
  position: relative;
  cursor: pointer;
}

.portfolio-box-01 .portfolio-info {
  width: 100%;
    position: absolute;
    left: 0;
    bottom: -40px;
    text-align: center;
    visibility: hidden;
    opacity: 0;
    z-index: 9;
    transition: .3s ease-in-out;
    padding: 30px;
    height: 100px;
}

.portfolio-box-01:hover .portfolio-info {
  
background: #0000008a;
  visibility: visible;
  opacity: 7;
  transform: translateY(-40px);
  transition: .3s ease-in-out;
  z-index: 30;
}

.link-box {
  text-align: center;
  border: 1px solid #ccc;
  display: flex;
  align-items: center;
  padding: 0 10px;
}

.link-box:hover {
  background: #ccc;
}
</style>
