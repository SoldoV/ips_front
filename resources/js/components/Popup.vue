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

<style>
.popup {
  position: fixed;
  background: #262626d0;
  mix-blend-mode: normal;
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
}
.card {
  box-sizing: border-box;
  padding: 18px 65px 38px 65px;
  width: 570px;
  background: #ffffff;
  box-shadow: 0px 0px 60px rgba(0, 0, 0, 0.5);
}
.card__label {
  display: block;
  position: relative;
  top: -37px;
  left: 11px;
  z-index: 1;
  transition: all 0.3s ease-out;
  font-weight: 300;
  font-size: 18px;
  line-height: 22px;
  color: #828282;
}
.card__input {
  box-sizing: border-box;
  padding: 8.5px 0 0 11px;
  display: block;
  position: relative;
  background: none;
  border: none;
  box-shadow: inset 0px 1px 5px rgba(142, 142, 142, 0.5);
  width: 100%;
  min-height: 54px !important;
  max-height: 54px !important;
  font-size: 16px;
  z-index: 2;
  font-weight: 300;
  font-size: 16px;
  line-height: 19px;
  color: #000000;
}

.card__input:focus,
.card__input:valid {
  outline: none;
  border: 1px solid #9e9e9e;
}
c .card__input:focus + .card__label,
.card__input:valid + .card__label {
  top: -50px;
  font-size: 12px;
}
.card__close {
  float: right;
  position: relative;
  left: 54px;
  top: -7px;
  cursor: pointer;
}
.card__header {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.card__text {
  font-weight: bold;
  font-size: 23px;
  line-height: 28px;
  text-align: center;
  color: #464646;
  margin-bottom: 23px;
}
.card__text--highlight {
  color: #007a02;
  display: inline-block;
  margin: 0 5px 0 5px;
}
.card__line {
  background: url("../../../public/images/imgs/progress.svg");
  width: 220px;
  height: 2px;
}
.card__line--unfinished {
  width: 220px;
  height: 2px;
  background-color: #e5e5e5;
}

.card__progress {
  display: flex;
  flex-direction: row;
  margin: 11px 0 22px 0;
}
.card__button {
  width: 100% !important;
  height: 48px !important;
  margin-top: 0px !important;
  font-weight: bold !important;
  font-size: 18px !important;
}
.card__step {
  font-size: 14px;
  color: rgba(0, 0, 0, 0.5);
}
.card__input--error {
  border: 1px solid #e51323 !important;
  color: #e51323;
}
.card__label--error {
  color: #e51323;
}
</style>
