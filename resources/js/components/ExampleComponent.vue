<template>
  <div class="container">
    <div class="main">
      <div class="main__header">10 Best Photo Apps For Incredible iPhone Photography (2020 Edition)</div>
      <img src="../../../public/images/imgs/Divider.png" class="main__line">
      <p
        class="main__text"
      >How do you capture more interesting travel photos with your iPhone? How do you avoid taking the same cliché vacation photos that everyone else takes? I recently interviewed Steffen Geldner – a talented iPhone photographer with a passion for travel. In this article, Steffen reveals 7 tips for shooting beautiful travel photos that will preserve the amazing memories of your trip. Read on to discover how to take better travel photos with your iPhone!</p>
      <img
        class="main__image"
        src="../../../public/images/imgs/main__image.png"
        srcset="../../../public/images/imgs/main__image@2x.png 2x, ../../../public/images/imgs/main__image@3x.png 3x"
      >
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
        class="main__subheader main__second-subheader"
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
      <button @click="togglePopup()" class="sidebar__button">Send Me The Tips</button>
    </div>
    <popup v-if="popupOpen" @close="togglePopup()"/>
  </div>
</template>

<script>
import popup from "./Popup.vue";
export default {
  components: {
    popup
  },
  data: () => ({
    popupOpen: false
  }),
  methods: {
    togglePopup() {
      this.popupOpen = !this.popupOpen;
    }
  }
};
</script>

<style>
* {
  font-family: "Lato";
}
.main__line {
  height: 2px;
  width: 100%;
}
.main {
  width: 560px;
  margin-top: 76px;
  margin-bottom: 138px;
}
.sidebar {
  margin: 154px 0 0 70px;
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
  margin: 18px 0 18px 0;
  color: #101010;
}
.main__subtext {
  font-weight: 300;
  font-size: 16px;
  line-height: 24px;
  margin: 28px 0 28px 0;
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
  max-width: 100%;
  margin-bottom: 44px;
}
@media only screen and (max-width: 940px) {
  .container {
    flex-flow: column;
    align-items: center;
  }
  .main {
    width: 80%;
    margin-bottom: 0px;
  }
  .main__line {
    width: 100%;
  }
  .sidebar {
    height: 426px;
    width: 80%;
    margin: 11px 0 37px 0;
  }
}

@media only screen and (max-width: 560px) {
  .sidebar__button {
    font-size: 20px;
    height: 50px;
    width: 100%;
    margin: 34px 29px 0 29px;
  }
  .main__second-subheader {
    margin-top: 43px;
  }
  .main__text {
    margin: 22px 0 22px 0;
  }
  .main__image {
    margin-left: -18px;
    max-width: 100vw;
    margin-bottom: 31px;
  }
  .container {
    margin: 0 18px 0 18px;
  }
  .main__line {
    width: 100%;
  }
  .main {
    margin-top: 25px;
    width: 100%;
  }
  .sidebar {
    width: 100%;
  }
}
</style>
