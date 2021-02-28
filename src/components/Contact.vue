<template>
  <section id="contactus">
    <div class="container">
      <div class="row">
        <div class="col-md-5">
          <div class="contact-info">
            <h4>What’s your story? Get in touch</h4>
            <p>
              Always available for freelancing if the right project comes along,
              Feel free to contact me.
            </p>
            <p class="custom-span-contact position-relative">
              <i class="fa fa-envelope position-absolute"></i>
              <span class="d-block">mail me</span>ogochukwuodom@gmail.com
            </p>
            <p class="custom-span-contact position-relative">
              <i class="fa fa-phone position-absolute"></i>
              <span class="d-block">Call me</span>080-6748-88682
            </p>
            <p class="custom-span-contact position-relative">
              <i class="fa fa-map-marker position-absolute"></i>
              <span class="d-block">Find me</span>ogochukwuodom@gmail.com
            </p>
            <!-- <ul>
                                <li class="media">
                                    <i class="fa fa-eye"></i>
                                    <span class="media-body">123 Stree New York City , United States Of America 750065.</span>
                                </li>
                                <li class="media">
                                    <i class="ti-email"></i>
                                    <span class="media-body">support@domain.com</span>
                                </li>
                                <li class="media">
                                    <i class="ti-mobile"></i>
                                    <span class="media-body">+044 9696 9696 3636</span>
                                </li>
                            </ul> -->
          </div>
        </div>
        <div class="col-md-7">
          <div class="contact-form">
            <h4 class="mb-4">Say Something</h4>
            <form id="contact-form" @submit.prevent="sendMessage">
              <div class="row">
                <div class="col-md-6">
                  <div class="form-group">
                    <input
                      name="Name"
                      id="name"
                      placeholder="Name *"
                      v-model="formData.name"
                      class="form-control"
                      type="text"
                    />
                  </div>
                </div>
                <div class="col-md-6">
                  <div class="form-group">
                    <input
                      name="Email"
                      id="email"
                      placeholder="Email *"
                      v-model="formData.email"
                      class="form-control"
                      type="email"
                    />
                  </div>
                </div>
                <div class="col-12">
                  <div class="form-group">
                    <input
                      name="Subject"
                      id="subject"
                      placeholder="Subject *"
                      v-model="formData.subject"
                      class="form-control"
                      type="text"
                    />
                  </div>
                </div>
                <div class="col-md-12">
                  <div class="form-group">
                    <textarea
                      name="message"
                      id="message"
                      placeholder="Your message *"
                      v-model="formData.message"
                      rows="5"
                      class="form-control"
                    ></textarea>
                  </div>
                </div>
                <div class="col-md-12">
                  <div class="send">
                    <button
                      class="btn btn-warning font-weight-bold"
                      type="submit"
                      value="Send"
                    >
                      Send Message
                    </button>
                  </div>
                  <span
                    id="suce_message"
                    class="text-success"
                    style="display: none"
                    >Message Sent Successfully</span
                  >
                  <span
                    id="err_message"
                    class="text-danger"
                    style="display: none"
                    >Message Sending Failed</span
                  >
                </div>
              </div>
            </form>
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
      formData: {}
    }
  },
  methods: {
    sendMessage() {
      console.log(this.formData)
      this.formData = ""
    }
  }
};
</script>

<style scoped>
#contactus {
  padding: 100px 0 50px;
}

.d-block {
  display: block;
}

.custom-span-contact {
  /* font-weight: 600; */
  padding-left: 50px;
  line-height: 21px;
  padding-top: 5px;
}

.custom-span-contact i {
  left: 0;
  top: 10px;
  font-size: 33px;
}

 @media(max-width: 900px){
        .contact-form {
            margin-top: 40px;
        }
    }
</style>
