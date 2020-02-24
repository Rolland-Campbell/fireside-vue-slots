<template>
  <div class="modal" :id="id" tabindex="-1" role="dialog">
    <div class="modal-dialog" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">
            <!-- slot added for input, named slot -->
            <slot name="title"></slot>
          </h5>
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
        <div class="modal-body">
          <!-- slot added for input -->
          <slot name="body"></slot>
        </div>
        <div class="modal-footer">
          <h5>Neato!</h5>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "modal-one",
  data() {
    return {};
  },
  props: ["id"],
  computed: {},
  methods: {},
  components: {}
};
</script>


<style scoped>
</style>