<template>
  <div class="md-layout-item md-medium-size-33 md-small-size-100">
    <div class="team-player">
      <md-card class="md-card-plain">
        <div class="md-layout-item md-size-50 mx-auto">
          <img
            :src="src"
            alt="Thumbnail Image"
            class="img-raised rounded-circle img-fluid"
          />
        </div>
        <h4 class="card-title">
          {{ name }}
          <br />
          <small class="card-description text-muted">{{ position }}</small>
        </h4>

        <md-card-content>
          <p class="card-description">
            {{ description }}
          </p>
        </md-card-content>

        <md-card-actions class="text-center">
          <md-button href="javascript:void(0)" class="md-just-icon md-simple">
            <i class="fab fa-twitter"></i>
          </md-button>
          <md-button href="javascript:void(0)" class="md-just-icon md-simple">
            <i class="fab fa-instagram"></i>
          </md-button>
          <md-button href="javascript:void(0)" class="md-just-icon md-simple">
            <i class="fab fa-facebook-square"></i>
          </md-button>
        </md-card-actions>
      </md-card>
    </div>
  </div>
</template>

<script>
export default {
  setup() {},
  props: {
    src: String,
    name: String,
    position: String,
    description: String,
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