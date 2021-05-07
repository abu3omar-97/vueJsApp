<template>
  <div class="wrapper">
    <parallax class="section page-header header-filter" :style="headerStyle">
      <div class="container">
        <div class="md-layout">
          <div
            class="md-layout-item md-size-50 md-small-size-70 md-xsmall-size-100"
          >
            <h1 class="title">Welcome To Our World Of Fun</h1>
            <h4>
              Design is intelligence made visible. All the mapping
              features most developers ever need, it is designed with
              simplicity, performance and usability in mind. Built Using Vue JS and Material Design
            </h4>
            <br />
            <md-button href="" class="md-success md-lg" target="_blank"
              ><i class="fab fa-vuejs"></i> Welcome</md-button
            >
          </div>
        </div>
      </div>
    </parallax>
    <div class="main main-raised">
      <div class="section">
        <div class="container">
          <div class="md-layout">
            <div
              class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto text-center"
            >
              <h2 class="title text-center">Let's talk product</h2>
              <h5 class="description">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Temporibus facere quam numquam itaque ad aperiam dicta nihil,
                repellendus ducimus odio similique eligendi, laudantium
                doloribus.
              </h5>
            </div>
          </div>
          <div class="features text-center">
            <div class="md-layout">
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="info">
                  <div class="icon icon-info">
                    <md-icon>chat</md-icon>
                  </div>
                  <h4 class="info-title">Support</h4>
                  <p>
                    - Cross Platform Mobile Applications (Flutter) - Building
                    websites using trend technologies - Maintaining websites
                    using Joomla and WordPress - Projects for individuals on
                    freelancing platforms - Graphic Designs
                  </p>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="info">
                  <div class="icon icon-success">
                    <md-icon>verified_user</md-icon>
                  </div>
                  <h4 class="info-title">Trust</h4>
                  <p>
                    - Cross Platform Mobile Applications (Flutter) - Building
                    websites using trend technologies - Maintaining websites
                    using Joomla and WordPress - Projects for individuals on
                    freelancing platforms - Graphic Designs
                  </p>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="info">
                  <div class="icon icon-danger">
                    <md-icon>fingerprint</md-icon>
                  </div>
                  <h4 class="info-title">Secured</h4>
                  <p>
                    - Cross Platform Mobile Applications (Flutter) - Building
                    websites using trend technologies - Maintaining websites
                    using Joomla and WordPress - Projects for individuals on
                    freelancing platforms - Graphic Designs
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="section text-center">
        <div class="container">
          <h2 class="title">Here is our team</h2>

          <div class="team">
            <div class="md-layout">
              <TeamMember
                :src="teamImg1"
                name="Yaman Alashqar"
                position="Computer Scientist"
                description="I am a 23-year-old, “Computer Scientist”, who never loses the desire to learn and improve his talents.
I always look for new challenges, those which will make best use of my existing skills and experience and also further my development and knowledge."
              />
              <TeamMember
                :src="teamImg2"
                name="Mousa Sandoqa"
                position="GIS Developer"
                description="I am a 23-year-old, “GIS Developer”, who never loses the desire to learn and improve his talents.
I always look for new challenges, those which will make best use of my existing skills and experience and also further my development and knowledge."
              />
            </div>
          </div>
        </div>
      </div>
      <div class="section section-contacts">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto">
              <h2 class="text-center title">Get In Touch</h2>
              <h4 class="text-center description">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad ea
                deleniti ipsum, consequuntur distinctio commodi, vero cupiditate
                porro fugit ex perferendis.
              </h4>
              <form class="contact-form">
                <div class="md-layout">
                  <div class="md-layout-item md-size-50">
                    <md-field>
                      <label>Your Name</label>
                      <md-input v-model="name" type="text"></md-input>
                    </md-field>
                  </div>
                  <div class="md-layout-item md-size-50">
                    <md-field>
                      <label>Your Email</label>
                      <md-input v-model="email" type="email"></md-input>
                    </md-field>
                  </div>
                </div>
                <md-field maxlength="5">
                  <label>Your Message</label>
                  <md-textarea v-model="message"></md-textarea>
                </md-field>
                <div class="md-layout">
                  <div class="md-layout-item md-size-33 mx-auto text-center">
                    <md-button class="md-success">Send Message</md-button>
                  </div>
                  <Modal />
                </div>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TeamMember from "./components/TeamMember.vue";
import Modal from "./components/Modal";
export default {
  components: {
    TeamMember,
    Modal,
  },
  bodyClass: "landing-page",
  props: {
    header: {
      type: String,
      default: require("@/assets/img/bg7.jpg"),
    },
    teamImg1: {
      type: String,
      default: require("@/assets/img/faces/Yaman.jpg"),
    },
    teamImg2: {
      type: String,
      default: require("@/assets/img/faces/Mousa.jpg"),
    },
    teamImg3: {
      type: String,
      default: require("@/assets/img/faces/Yaman.jpg"),
    },
  },
  data() {
    return {
      name: null,
      email: null,
      message: null,
    };
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`,
      };
    },
  },
};
</script>

<style lang="scss" scoped>
.md-card-actions.text-center {
  display: flex;
  justify-content: center !important;
}
.contact-form {
  margin-top: 30px;
}

.md-has-textarea + .md-layout {
  margin-top: 15px;
}

.page-header h4,
.page-header h1 {
  text-shadow: 2px 2px 2px #616161;
}
</style>
