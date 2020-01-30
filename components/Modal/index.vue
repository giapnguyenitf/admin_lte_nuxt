<template>
  <transition name="fade">
    <div @click="$emit('close')" class="modal-container modal fade">
      <div @click.stop class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <button
              @click="$emit('close')"
              type="button"
              class="close"
              aria-label="Close"
            >
              <span aria-hidden="true">&times;</span>
            </button>
            <slot name="header">
              <h4 class="modal-title">Default Modal</h4>
            </slot>
          </div>
          <div class="modal-body">
            <slot name="body">
              <p>One fine body&hellip;</p>
            </slot>
          </div>
          <div class="modal-footer">
            <slot name="footer">
              <button
                @click="$emit('close')"
                type="button"
                class="btn btn-default pull-left"
              >
                Close
              </button>
              <button
                @click="$emit('close')"
                type="button"
                class="btn btn-primary"
              >
                Save changes
              </button>
            </slot>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {}
</script>
