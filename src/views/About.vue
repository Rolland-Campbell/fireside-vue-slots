<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div class="row justify-content-center">
      <!-- brought back title withe named slot property, same modal, simple styling -->
      <button class="btn btn-danger" data-toggle="modal" data-target="#three">Modal three</button>
      <ModalOne id="three">
        <div slot="title" class="modalThree">
          <i class="fas fa-dragon mr-3"></i>I brought back the title!
        </div>
        <div slot="body"><h5>Same modal, even more stuff</h5></div>
        <br />
        <!-- added an input to the modal layout -->
        <input class="mt-5" type="text" placeholder="Input field?.. what the..." v-model="message" />
      </ModalOne>
    </div>
    <div>
      <p class="mt-5">{{ message }}</p>
    </div>
    <div slot="body"><h2>Not ANOTHER modal!!</h2></div>
    <div class="row justify-content-center">
      <button class="btn btn-info" data-toggle="modal" data-target="#four">Modal four</button>
      <!-- bringing in modal again, adding title and a card to it -->
      <ModalOne id="four">
        <div slot="title">
          <h2>NEAT! a card</h2>
        </div>
        <!-- Let's add a card to our modal-->
        <div slot="body">
        <h3>HERE IT IS!!</h3>
        <div class="card" style="width: 18rem;">
          <img class="card-img-top" src="../assets/robot.png" alt="Card image cap" />
          <div class="card-body">
            <h5 class="card-title">Cool Card</h5>
            <p class="card-text">I used the same modal, but added a card!</p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
          </div>
        </div>
        </div>
      </ModalOne>
    </div>
  </div>
</template>

<script>
import ModalOne from "../components/Modal-One";
export default {
  name: "about",
  data() {
    return {
      message: ""
    };
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

h3{
  color: red;
  animation: blink 1s infinite
}

@keyframes blink {
  from {
    color: red
  }
  to{
    color:yellow
  }
  
}

</style>