<template>
  <div class="popup">
    <div class="card">
      <img class="card__close" @click="close()" src="../../../public/images/imgs/x.svg">
      <div class="card__header">
        <div class="card__step">Step 1 of 2</div>
        <div class="card__progress">
          <div class="card__line"></div>
          <div class="card__line--unfinished"></div>
        </div>
      </div>
      <div class="card__text">
        Enter Your Email To Get
        <div class="card__text--highlight">FREE</div>iPhone Photography Email Tips:
      </div>
      <input
        v-bind:class="{ 'card__input--error': !valid }"
        class="card__input"
        name="input"
        v-model="inputMail"
        type="text"
        required
        autocomplete="off"
      >
      <label
        v-bind:class="{ 'card__label--error': !valid }"
        class="card__label"
        for="input"
      >{{labelText}}</label>
      <button @click="validateForm()" class="card__button sidebar__button">Send Me The Tips »</button>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    valid: true,
    inputMail: "",
    labelText: "Please enter your email here"
  }),
  methods: {
    close() {
      this.$emit("close");
    },
    validateForm() {
      if (!/^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(this.inputMail)) {
        this.labelText = "Please enter a valid email adress";
        this.valid = false;
      } else {
        this.labelText = "Please enter your email here";
        this.valid = true;
        this.close();
      }
    }
  }
};
</script>

<style lang="scss">
@import "../../sass/_popup.scss";
</style>
