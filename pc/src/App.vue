<template>
  <div id="container">
    <div id="app">
      <section class="scrollsection" ref="ss1">
        <Newspaper v-on:callVisibilityChange="changeOverlayVisibility" />
        <div id="overlay" ref="overlay" class="visible">
        </div>
        <div ref="section" class="visible">
          <ActualSection v-on:callVisibilityChange="changeOverlayVisibility" />
        </div>
      </section>
      <section class="scrollsection" id="section2">
        <AboutSection />
      </section>
      <div class="sections-menu">
        <span class="menu-point" v-bind:class="{ active: activeSection == index }" v-on:click="scrollToSection(index)"
          v-for="(offset, index) in offsets" v-bind:key="index" v-bind:title="'Go to section ' + (index + 1)">
        </span>
      </div>
    </div>
  </div>
</template>

<script>
import Newspaper from "./components/Newspaper.vue";
import ActualSection from "./components/ActualSection.vue";
import AboutSection from "./components/AboutSection.vue";

export default {
  name: 'App',
  components: {
    Newspaper,
    ActualSection,
    AboutSection,
  },
  data() {
    return {
      inMove: false,
      inMoveDelay: 400,
      activeSection: 0,
      offsets: [],
      touchStartY: 0,
    };
  }, methods: {
    calculateSectionOffsets() {
      const sections = document.querySelectorAll('section');
      sections.forEach((section) => {
        this.offsets.push(section.offsetTop);
      });
    },
    handleMouseWheel(e) {
      if (e.deltaY > 0 && !this.inMove) {
        this.moveUp();
      } else if (e.deltaY < 0 && !this.inMove) {
        this.moveDown();
      }
      e.preventDefault();
    },
    moveDown() {
      this.inMove = true;
      this.activeSection--;
      if (this.activeSection < 0) this.activeSection = this.offsets.length - 1;
      this.scrollToSection(this.activeSection, true);
    },
    moveUp() {
      this.inMove = true;
      this.activeSection++;
      if (this.activeSection > this.offsets.length - 1) this.activeSection = 0;
      this.scrollToSection(this.activeSection, true);
    },
    scrollToSection(id, force = false) {
      if (this.inMove && !force) return false;
      this.activeSection = id;
      this.inMove = true;
      const section = document.querySelectorAll('section')[id];
      if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
      }
      setTimeout(() => {
        this.inMove = false;
      }, this.inMoveDelay);
    },
    changeOverlayVisibility() {
      this.$refs.overlay.classList.toggle("visible");
      this.$refs.section.classList.toggle("visible");

      this.$refs.overlay.classList.toggle("hidden");
      this.$refs.section.classList.toggle("hidden");
    },
    mobileCheck() {
      const isMobile = localStorage.mobile || window.navigator.maxTouchPoints > 1;
      return isMobile;
    },
  },
  mounted() {
    if (this.mobileCheck()) {
      window.location = "https://m.cnsh.dev";
    }
    this.calculateSectionOffsets();
    window.addEventListener('wheel', this.handleMouseWheel, { passive: false });
    window.addEventListener('touchstart', this.touchStart, { passive: false });
    window.addEventListener('touchmove', this.touchMove, { passive: false });
  },
  unmounted() {
    window.removeEventListener('wheel', this.handleMouseWheel, { passive: false });
    window.removeEventListener('touchstart', this.touchStart);
    window.removeEventListener('touchmove', this.touchMove);
  },
};
</script>

<style scoped>
#container {
  height: 100%;
  width: 100%;
}

#app {
  height: 100%;
  width: 100%;
}

#overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: url("./assets/overlay.png") repeat;
  backdrop-filter: blur(10px);
  z-index: 0;
}

#section2 {
  background: linear-gradient(-45deg, black, #debd9e);
  background-size: 200% 200%;
  width: 100%;
  height: 100vh;
  animation: animate 12s ease infinite;
  text-align: center;
}

.hidden {
  opacity: 0;
  visibility: hidden;
  transition: all 0.75s ease-out;
}

.visible {
  opacity: 1;
  visibility: visible;
  transition: all 0.75s ease-in;
}

.scrollsection {
  height: 100vh;
  width: 100%;
}

.sections-menu {
  position: fixed;
  right: 0.7rem;
  top: 50%;
  transform: translateY(-50%);
  mix-blend-mode: hard-light;
}

.sections-menu .menu-point {
  width: 10px;
  height: 10px;
  background-color: #362e2b;
  display: block;
  margin: 1rem 0;
  opacity: .6;
  transition: .4s ease all;
  border-radius: 50%;
}

.sections-menu .menu-point.active {
  opacity: 1;
  transform: scale(1.5);
}

.sections-menu .menu-point:hover {
  opacity: 1;
  transform: scale(1.2);
}

@keyframes animate {
  0% {
    background-position: 0 50%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0 50%;
  }
}
</style>