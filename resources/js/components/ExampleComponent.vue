<template>
  <div class="container">
    <div class="main">
      <div class="main__header">10 Best Photo Apps For Incredible iPhone Photography (2020 Edition)</div>
      <img src="../../../public/images/line.svg" class="main__line">
      <p
        class="main__text"
      >How do you capture more interesting travel photos with your iPhone? How do you avoid taking the same cliché vacation photos that everyone else takes? I recently interviewed Steffen Geldner – a talented iPhone photographer with a passion for travel. In this article, Steffen reveals 7 tips for shooting beautiful travel photos that will preserve the amazing memories of your trip. Read on to discover how to take better travel photos with your iPhone!</p>
      <img
        class="main__image"
        src="../../../public/images/main__image.png"
        srcset="../../../public/images/main__image@2x.png 2x, ../../../public/images/main__image@3x.png 3x"
      >
      <input type="text" name="input" required autocomplete="off">
      <label for="input">Please enter your email here</label>
      <div class="main__subheader">1. Research Your Destination To Find The Best Photo Opportunities</div>
      <p
        class="main__text"
      >Before your trip, I recommend researching the destination to find the most interesting photo opportunities.</p>
      <p
        class="main__text"
      >I always research the location I’m traveling to. I do this extensively and obsessively!</p>
      <p
        class="main__text"
      >It’s up to you how much research you do. But you should definitely spend a bit of time looking up some great places to take pictures.</p>
      <p class="main__text">So, what kind of research can you do?</p>
      <p
        class="main__text"
      >First, you could search for photos that other people have taken at the locations you’re planning to visit.</p>
      <p
        class="main__text"
      >Search on Instagram or Google to get an idea of the kinds of photos people take there.</p>
      <div
        class="main__subheader"
      >2. Capture Your Journey To Tell The Complete Story Of Your Travels</div>
      <p class="main__text">Travel photography isn’t just about photographing the destination.</p>
      <p
        class="main__text"
      >For a more complete photographic story, capture your journey to and from the location you’re visiting.</p>
      <p
        class="main__text"
      >If you’re traveling by plane, try to get a window seat where you have a view of the wing or propeller.</p>
      <p
        class="main__text"
      >And of course, you could capture a beautiful aerial view of clouds, mountains, or city lights as you’re flying above.</p>
      <p
        class="main__text"
      >Your journey will often involve several different types of transport. And they all offer great photo opportunities.</p>
      <p
        class="main__text"
      >Whether you’re traveling by car, taxi, bus, train, boat, or plane, try to capture some interesting photos.</p>
    </div>
    <div class="sidebar">
      <button class="sidebar__button">Send Me The Tips »</button>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    console.log("Component mounted.");
  }
};
</script>

<style>
* {
  font-family: "Lato";
}
.main {
  width: 560px;
}
.sidebar {
  margin-left: 70px;
  width: 270px;
  height: 640px;
  background-color: #f5f5f5;
  display: flex;
  justify-content: center;
}
.container {
  display: flex;
  flex-flow: row;
  justify-content: center;
}
.main__header {
  font-style: normal;
  font-weight: bold;
  font-size: 26px;
  line-height: 31px;
  color: #101010;
}
.main__text {
  font-weight: 300;
  font-size: 16px;
  line-height: 24px;
  color: #101010;
}
.main__subheader {
  font-weight: bold;
  font-size: 18px;
  line-height: 22px;
  color: #101010;
}
.sidebar__button {
  background: linear-gradient(90deg, #ac519c 0.83%, #e5424f 100%);
  box-shadow: 0px 3px 10px rgba(104, 104, 104, 0.5);
  width: 220px;
  height: 40px;
  font-weight: bold;
  font-size: 15px;
  line-height: 18px;
  color: #ffffff;
  border: none !important;
  margin-top: 50px;
}
.sidebar__button:hover {
  background: linear-gradient(90deg, #b678aa 1.29%, #e28990 100%);
}
.main__image {
  width: 100%;
  height: 331px;
}

label {
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

input {
  box-sizing: border-box;
  padding: 8.5px 0 0 11px;
  display: block;
  position: relative;
  background: none;
  border: 1px solid #9e9e9e;
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

input:focus,
input:valid {
  outline: none;
}

input:focus + label,
input:valid + label {
  top: -54px;
  font-size: 12px;
}
</style>
