<template>
  <div class="about">
    <h1>This is an about page</h1>
    <!-- brought back title withe named slot property, simple styling -->
    <button class="btn btn-danger" data-toggle="modal" data-target="#three">Modal three</button>
    <ModalOne id="three">
      <div slot="title" class="modalThree">
        <i class="fas fa-dragon mr-3"></i>I brought back the title!
      </div>
      <h5>Same modal, even more stuff</h5>
      <br />
      <!-- added a change to the modal layout -->
      <input class="mt-5" type="text" placeholder="Input field?.. what the..." />
    </ModalOne>
  </div>
</template>

<script>
import ModalOne from "../components/Modal-One";
export default {
  name: "about",
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: { ModalOne }
};
</script>


<style scoped>
.modalThree {
  color: blue;
  font-style: italic;
}
</style>