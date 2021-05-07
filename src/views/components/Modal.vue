<template>
      <div class="md-layout-item md-size-33 mx-auto text-center">
              <md-button
                class="md-success md-block"
                @click="classicModal = true"
                ><md-icon>library_books</md-icon> Modal</md-button
              >
              <modal v-if="classicModal" @close="classicModalHide">
                <template slot="header">
                  <h4 class="modal-title">Modal Title</h4>
                  <md-button
                    class="md-simple md-just-icon md-round modal-default-button"
                    @click="classicModalHide"
                  >
                    <md-icon>clear</md-icon>
                  </md-button>
                </template>

                <template slot="body">
                  <p>
                   Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsam corrupti soluta deleniti id voluptatum minima itaque eveniet mollitia odit obcaecati optio, minus ad repellat consequatur, totam aliquam officiis illum voluptates!
                  </p>
                </template>

                <template slot="footer">
                  <md-button class="md-simple">Button</md-button>
                  <md-button
                    class="md-danger md-simple"
                    @click="classicModalHide"
                    >Close</md-button
                  >
                </template>
              </modal>
      </div>
</template>

<script>
import { Modal } from "@/components";
export default {
  components: {
    Modal
  },
  data() {
    return {
      classicModal: false,
    };
  },
  methods: {
    classicModalHide() {
      this.classicModal = false;
    }
  }
};
</script>
