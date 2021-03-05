<template>
  <section id="resume">
      <div class="container">
          <div class="title">
              <h3>Experience</h3>

          </div>
          <div class="resume-box">
              <div class="resume-row" v-for="(userExp, index) in userExperience" :key="index">
                  <div class="row">
                      <div class="col-md-3">
                          <div class="rb-left">
                                <h6>{{userExp.role}}</h6>
                                <label>{{userExp.company}} | {{userExp.nature}}</label>
                                <p class="mt-1 mb-2">{{userExp.duration}}</p>
                                <div class="rb-time">{{userExp.time}}</div>
                            </div>
                      </div>
                      <div class="col-md-9">
                            <div class="rb-right">
                                <h6>About Company</h6>
                                <p>{{userExp.about}}</p>
                            </div>
                      </div>
                  </div>
              </div>
          </div>
      </div>

  </section>
</template>

<script>
export default {
    data() {
        return {
            userExperience: [ 
                {
                role: 'Front-end Developer',
                company: 'Kodehauz',
                nature: 'On-site',
                duration: 'Jan 2019 - Present',
                time: 'Full Time',
                about: "It is located in Eket Akwa Ibom state. It's vision is to create a flourishing ecosystem powered by"
            },
                {
                role: 'Front-end Developer',
                company: 'Next Inn',
                nature: 'Remote',
                duration: 'Jan 2019 - Present',
                time: 'Full Time',
                about: "A company started up to fill the gap of unemployment while sharpwning up the developer's skill. The tech stack was HTMl, Css, JavaScript, Handlebars, Node JS, Vue, Nuxt"
            },
                {
                role: 'Front-end Developer',
                company: 'HNG',
                nature: 'Remote',
                duration: 'Jan 2019 - Present',
                time: 'Part Time',
                about: "An internship where the best of developers are selelcted after a battlw royal for a couple od weeks. It comprises of ten stages of which developers are evicted as the day goes. The watch word goes sleep is for the weak. you have to always be a scout cos, tasks can get dropped anytime."
            },
                {
                role: 'Writer',
                company: 'Silver Lining',
                nature: 'On-site',
                duration: 'Jan 2019 - Present',
                time: 'Full Time',
                about: "A firm for novel writing. I wrote my novels in this firm. It's not the regular firm with a building but a firm in my heart."
            },
            ]
        }
    }
}
</script>

<style scoped>

    #resume {
        padding: 100px 0;
    }
    .resume-row {
        background: #0b0b13;
        padding: 35px;
        border-radius: 15px;
    }

    .resume-row + .resume-row {
        margin-top: 30px;
    }

    .resume-row .rb-left {
        border-right: 1px solid rgba(255, 255, 255, 0.05);
    }

    .resume-row h6 {
        color: #fff;
        font-weight: 500;
        font-size: 20px;
    }

    .resume-row .label {
        font-size: 14px;
        font-style: italic;
    }

    .rb-time {
        padding: 5px 10px;
        border-radius: 3px;
        color: #fff;
        background: #ff9301;
        font-size: 12px;
        font-weight: 500;
        display: inline-block;
    }

     @media(max-width: 900px){
        .rb-right {
            margin-top: 30px;
        }
    }
</style>