<template>
  <div>
    <breadcrumb
      :pageHeader="'Dashboard'"
      :optionalDescription="'Control panel'"
      :level="'Home'"
      :activeLevel="'Dashboard'"
    ></breadcrumb>
    <section class="content">
      <div class="callout callout-info">
        <h4>Reminder!</h4>
        Instructions for how to use modals are available on the
        <a href="http://getbootstrap.com/javascript/#modals"
          >Bootstrap documentation</a
        >
      </div>

      <div class="row">
        <div class="col-xs-12">
          <div class="box box-default">
            <div class="box-header with-border">
              <h3 class="box-title">Modal Examples</h3>
            </div>
            <div class="box-body">
              <button
                @click="openModal()"
                type="button"
                class="btn btn-default"
              >
                Launch Default Modal
              </button>
            </div>
          </div>
        </div>
        <modal v-show="showModal" :class="{ in: showModal }" @close="close()">
          <h4 slot="header" class="modal-title">Default Modal vue</h4>
          <p slot="body">Default body vuejs&hellip;</p>
        </modal>
      </div>
    </section>
  </div>
</template>

<style>
.modal {
  display: block;
}

.modal-open {
  padding-right: 15px;
}
</style>

<script>
import Breadcrumb from '~/layouts/Breadcrumb'
import Modal from '~/components/Modal/index'

export default {
  layout: 'Master',
  components: {
    Breadcrumb,
    Modal
  },
  data() {
    return {
      showModal: false
    }
  },
  methods: {
    close() {
      this.showModal = false
      document.body.classList.remove('modal-open')
    },
    openModal() {
      this.showModal = true
      document.body.classList.add('modal-open')
    }
  }
}
</script>
