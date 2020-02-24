<template>
  <div class="home">
    <div class="row logoRow">
      <h3>Modal</h3>
      <img alt="Vue logo" src="../assets/logo.png" class="logo" />
      <h3>iew</h3>
    </div>
    <div class="row buttons">
      <button class="btn btn-primary" data-toggle="modal" data-target="#one">Modal one</button>
      <button class="btn btn-warning" data-toggle="modal" data-target="#two">Modal two</button>
    </div>
    <ModalOne id="one">
      <div slot="title">some title</div>
      <div slot="body">STUFF HERE</div>
    </ModalOne>
    <ModalOne id="two">
      <div slot="body">no title? same modal, more STUFF</div>
      </ModalOne>
  </div>
</template>

<script>
// @ is an alias to /src
import ModalOne from "../components/Modal-One";

export default {
  name: "home",
  components: { ModalOne }
};
</script>
<style scoped>
.logo {
  height: 30px;
  width: 30px;
}
.logoRow {
  justify-content: center;
}
.cardPos {
  justify-content: center;
  padding: 10px;
}
.buttons {
  justify-content: space-evenly;
  padding: 10px;
}
</style>
