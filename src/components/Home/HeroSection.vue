<template>
  <div id="carousel-wrapper">
    <div id="menu" :style="{ background: currentColor }">
      <div id="current-option">
        <span id="current-option-text1" :data-previous-text="previousText1" :data-next-text="nextText1">{{ currentText1 }}</span>
        <span id="current-option-text2" :data-previous-text="previousText2" :data-next-text="nextText2">{{ currentText2 }}</span>
      </div>
          <div id="image2" :style="{ backgroundImage: 'url(' + currentImage + ')' }"></div>
      <button id="previous-option" @click="previousOption"></button>
      <button id="next-option" @click="nextOption"></button>
    </div>
    <div id="image" :style="{ backgroundImage: 'url(' + currentImage + ')' }"></div>
  </div>
</template>

<script>
export default {
  name: "HeroSection",
  data() {
    return {
      currentIndex: 0,
      text1Options: [
        "The Realities of Forex Trading: Patience, Discipline, and Humility",
        "Webinar Financial Management: ICAEW tutor Christian Papworth reviews the Financial Management module.",
        "Assert Yourself: Believe in Your Abilities and Stand Strong",
        "The Power of High Expectations, High expectations are the key to everything",
        "Start Doing: Actions Speak Louder Than Words"
      ],
      text2Options: [
        "June 28, 2024. " + "Financial Management, " + "Personal Financial Advisor for WellsFargo. ",
        "June 26, 2024. " + "Financial Advisory, " + "Financial Management. ",
        "June 23, 2024. " + "Financial Advisory, " + "Financial Management. ",
        "June 23, 2024. " + "Financial Advisory, " + "Financial Management. ",
        "June 23, 2024. " + "Financial Advisory, " + "Financial Management. ",
      ],
      colorOptions: ["#e5e5ea", "#fdf7f4", "#e5e5ea", "#fdf7f4", "#e5e5ea"],
      imageOptions: [
        "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/1883851332-8ab9ed31ae8a858c13bf43d9faf3d6b40af4f76b2312973a05eebadcf1a5177a-d_1920x1080-1200x600.jpeg",
        "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/1884735154-723a272c15d7e97b9d2469f82cce2061d5a1f2dd9334209e95a6918641647e5d-d_1920x1080-1200x600.jpeg",
        "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/1878580167-62a459e9fd685b5ac06aa4d3a031a15b067bdbe63cbd067161cbf6e9d88a5f19-d_1920x1080-1200x600.jpeg",
        "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/1878555245-3b7bd894982e489fde36e428d21e470bd7612f3d2bb5a2ff8125dbf4aae7b6e8-d_1920x1080-1200x600.jpeg",
        "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/1878575645-0ab3e38180d61870ff8b00df96205fd9875e1578b3475c132782f7c7b0ae6aed-d_1920x1080-1200x600.jpeg"
      ],
      autoRotateInterval: null
    };
  },
  computed: {
    currentText1() {
      return this.text1Options[this.currentIndex];
    },
    currentText2() {
      return this.text2Options[this.currentIndex];
    },
    currentColor() {
      return this.colorOptions[this.currentIndex];
    },
    currentImage() {
      return this.imageOptions[this.currentIndex];
    },
    nextText1() {
      return this.text1Options[(this.currentIndex + 1) % this.text1Options.length];
    },
    nextText2() {
      return this.text2Options[(this.currentIndex + 1) % this.text2Options.length];
    },
    previousText1() {
      return this.text1Options[(this.currentIndex - 1 + this.text1Options.length) % this.text1Options.length];
    },
    previousText2() {
      return this.text2Options[(this.currentIndex - 1 + this.text2Options.length) % this.text2Options.length];
    }
  },
  mounted() {
    this.autoRotateInterval = setInterval(() => {
      this.nextOption();
    }, 10000); // Rotate every 10000 milliseconds (10 seconds)
  },
  beforeUnmount() { // Use `beforeDestroy` if you're using Vue 2
    clearInterval(this.autoRotateInterval);
  },
  methods: {
    nextOption() {
      this.currentIndex = (this.currentIndex + 1) % this.text1Options.length;
      this.animateCarousel("next");
    },
    previousOption() {
      this.currentIndex = (this.currentIndex - 1 + this.text1Options.length) % this.text1Options.length;
      this.animateCarousel("previous");
    },
    animateCarousel(direction) {
      const carousel = this.$el.querySelector("#carousel-wrapper");
      if (carousel) {
        carousel.classList.add(`anim-${direction}`);
        setTimeout(() => {
          carousel.classList.remove(`anim-${direction}`);
        }, 650);
      }
    }
  }
}
</script>



<style scoped>
#carousel-wrapper {
  width: auto;
  height: auto;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
}

#carousel-wrapper #menu {
  height: 470px;
  width: 100%;
  overflow: hidden;
  font-weight: 700;
  line-height: 1;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  vertical-align: middle;
  transition: all 0.6s ease-in-out;
}

#carousel-wrapper #menu #current-option {
  position: relative;
  width: 100%;
  height: 100%;
  transform: translate(-20%, 0%);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

#carousel-wrapper #menu #current-option #current-option-text1 {
  font-size: 2rem;
  line-height: 2.4rem;
  width: 550px;
  height: 200px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  font-family: 'BR-Firma-Bold', sans-serif;
}

#carousel-wrapper #menu #current-option #current-option-text1::before {
  content: attr(data-next-text);
  position: absolute;
  transform: translate(0%, 380px);
  width: 100%;
  height: 200px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
}

#carousel-wrapper #menu #current-option #current-option-text1::after {
  content: attr(data-previous-text);
  position: absolute;
  transform: translate(0%, -380px);
  width: 100%;
  height: 200px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
}

#carousel-wrapper #menu #current-option #current-option-text2 {
  font-size: 1rem;
  line-height: 1.7rem;
  width: 550px;
  height: 25px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-end;
}

#carousel-wrapper #menu #current-option #current-option-text2::before {
  content: attr(data-next-text);
  position: absolute;
  transform: translate(0%, 380px);
  width: 100%;
  height: 40px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-end;
}

#carousel-wrapper #menu #current-option #current-option-text2::after {
  content: attr(data-previous-text);
  position: absolute;
  transform: translate(0%, -380px);
  width: 100%;
  height: 40px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-end;
}

#carousel-wrapper #menu #previous-option,
#carousel-wrapper #menu #next-option {
  width: 1.5rem;
  height: 1.5rem;
  border: none;
  display: block;
  cursor: pointer;
  background-size: cover;
  position: absolute;
}

#carousel-wrapper #menu #previous-option {
  background: url("data:image/svg+xml,%3Csvg version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' x='0px' y='0px' viewBox='0 0 256 256'%3E%3Cpolygon points='225.813,48.907 128,146.72 30.187,48.907 0,79.093 128,207.093 256,79.093' fill='%23333'%3E%3C/polygon%3E%3C/svg%3E");
  transform: translate(480px, 50px);
}

#carousel-wrapper #menu #next-option {
  background: url("data:image/svg+xml,%3Csvg version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' x='0px' y='0px' viewBox='0 0 256 256'%3E%3Cpolygon points='225.813,48.907 128,146.72 30.187,48.907 0,79.093 128,207.093 256,79.093' fill='%23333'%3E%3C/polygon%3E%3C/svg%3E");
  transform: translate(480px, -50px) rotate(180deg);
}

#carousel-wrapper #image {
  height: 350px;
  width: 345px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  z-index: 101;
  position: absolute;
  transform: translate(250px, 0);
}

#carousel-wrapper.anim-next,
#carousel-wrapper.anim-previous {
  pointer-events: none;
}

#carousel-wrapper #image2 {
  height: 350px;
  width: 345px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  z-index: unset;
  position: unset;
  transform: unset;
  display: none;
}

@keyframes previous-text {
  50%,
  55% {
    transform: translate(0%, 390px);
  }
  to {
    transform: translate(0%, 380px);
  }
}

@keyframes previous-top-arrow {
  50% {
    transform: translate(310px, 53px);
  }
}

@keyframes previous-bottom-arrow {
  50% {
    transform: translate(310px, -47px) rotate(180deg);
  }
}

@keyframes previous-image {
  0% {
    transform: translate(140px, 0) scale(1);
    opacity: 1;
  }
  70% {
    transform: translate(140px, 0) scale(1.1);
    opacity: 0;
  }
  100% {
    transform: translate(140px, 0) scale(1);
    opacity: 1;
  }
}

@keyframes next-text {
  50%,
  55% {
    transform: translate(0%, -390px);
  }
  to {
    transform: translate(0%, -380px);
  }
}

@keyframes next-top-arrow {
  50% {
    transform: translate(310px, 47px);
  }
}

@keyframes next-bottom-arrow {
  50% {
    transform: translate(310px, -53px) rotate(180deg);
  }
}

@keyframes next-image {
  0% {
    transform: translate(140px, 0) scale(1);
    opacity: 1;
  }
  70% {
    transform: translate(140px, 0) scale(1.1);
    opacity: 0;
  }
  100% {
    transform: translate(140px, 0) scale(1);
    opacity: 1;
  }
}



@media (max-width: 990px) {

}

@media (max-width: 900px) {

  #carousel-wrapper #image {
    display: none;
  }

  #carousel-wrapper #menu #previous-option {
    display: none;
  }

  #carousel-wrapper #menu #next-option {
    display: none;
  }

  #carousel-wrapper #menu #current-option {
    position: relative;
    width: 100%;
    height: 100%;
    transform: unset;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    margin-top: 30px;
  }

  #carousel-wrapper #image2 {
    height: 650px;
    width: 545px;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    z-index: unset;
    position: unset;
    transform: unset;
    display: unset;
    margin-top: 25px;
    margin-bottom: 50px;
  }

  #carousel-wrapper #menu {
    height: 570px;
    width: 100%;
    overflow: hidden;
    font-weight: 700;
    line-height: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    vertical-align: middle;
    transition: all 0.6s ease-in-out;
  }

}

@media (max-width: 500px) {
  #carousel-wrapper #menu #current-option #current-option-text1 {
    font-size: 1.4rem;
    line-height: 2rem;
    width: 420px;
    height: 200px;
  }

  #carousel-wrapper #menu #current-option #current-option-text2 {
    font-size: 1rem;
    line-height: 1.7rem;
    width: 420px;
    height: 25px;
  }

  #carousel-wrapper #image2 {
    height: 650px;
    width: 420px;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    z-index: unset;
    position: unset;
    transform: unset;
    display: unset;
    margin-top: 25px;
    margin-bottom: 50px;
  }
}

</style>