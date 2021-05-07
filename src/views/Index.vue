<template>
  <div class="wrapper">
    <parallax class="section page-header header-filter" :style="headerStyle">
      <div class="container">
        <div class="md-layout">
          <div
            class="md-layout-item md-size-50 md-small-size-70 md-xsmall-size-100"
          >
            <h1 class="title">Landing Page</h1>
            <h4>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Blanditiis, odio pariatur. Placeat at accusantium repudiandae nam
              doloremque dolorum fugit fuga! Sunt facere veritatis harum facilis
              pariatur, maiores voluptatibus numquam! Officiis?
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
                doloribus. Tenetur eligendi culpa iusto at autem.
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
                  <h4 class="info-title">Yaman</h4>
                  <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Adipisci enim obcaecati repellat. Dignissimos doloremque
                    libero repudiandae nostrum molestias quos, totam aperiam.
                    Dolor dicta pariatur, ad ipsum voluptas nemo tempora.
                    Possimus?
                  </p>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="info">
                  <div class="icon icon-success">
                    <md-icon>verified_user</md-icon>
                  </div>
                  <h4 class="info-title">Yaman</h4>
                  <p>
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Nobis eveniet dolor voluptas facere, corporis est voluptates
                    placeat pariatur modi, numquam architecto, impedit vitae ea.
                    Molestias, commodi amet. Nobis, iste numquam.
                  </p>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="info">
                  <div class="icon icon-danger">
                    <md-icon>fingerprint</md-icon>
                  </div>
                  <h4 class="info-title">Yaman</h4>
                  <p>
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Molestias perferendis eius eligendi dolor nam est eum aut
                    tempore adipisci nisi vero enim ut consequatur rem, facere
                    voluptatum totam perspiciatis quam.
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
                position="Web Dev"
                description="Lorem ipsum dolor sit, amet consectetur Lorem ipsum dolor sit, amet consectetur adipisicing elit.  elit.  "
              />
              <TeamMember
                :src="teamImg2"
                name="Yaman Omar"
                position="Web Dev"
                description="test Lorem ipsum dolor sit, amet consectetur adipisicing elit.  "
              />
              <TeamMember
                :src="teamImg3"
                name="Yaman Omar Alashqar"
                position="Web Dev"
                description="Lorem ipsum dolor sit, amet consectetur adipisicing elit.  "
              />
            </div>
          </div>
        </div>
      </div>
      <div class="section section-contacts">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto">
              <h2 class="text-center title">Form Example</h2>
              <h4 class="text-center description">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad ea
                deleniti ipsum, consequuntur distinctio commodi, vero cupiditate
                porro fugit ex perferendis voluptatibus sequi nam voluptas sit,
                temporibus est aperiam blanditiis!
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
      default: require("@/assets/img/faces/Yaman.jpg"),
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
</style>
