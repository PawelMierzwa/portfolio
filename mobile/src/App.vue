<template>
  <div id="container">
    <div id="app">
      <div>
        <IntroductionSection/>
        <ProjectsSection/>
        <ContactSection/>
        <div class="sections-menu">
          <span class="menu-point" v-bind:class="{ active: activeSection == index }" v-on:click="scrollToSection(index)"
            v-for="(offset, index) in offsets" v-bind:key="index" v-bind:title="'Go to section ' + (index + 1)">
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import IntroductionSection from './components/IntroductionSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import ContactSection from './components/ContactSection.vue'

export default {
  name: 'App',
  components: {
    IntroductionSection,
    ProjectsSection,
    ContactSection,
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
    touchStart(e) {
      e.preventDefault();
      this.touchStartY = e.touches[0].clientY;
    },
    touchMove(e) {
      if (this.inMove || this.touchStartY === 0) return;
      e.preventDefault();
      const currentY = e.touches[0].clientY;
      if (this.touchStartY < currentY) {
        this.moveDown();
      } else {
        this.moveUp();
      }
      this.touchStartY = 0;
    }
  },
  mounted() {
    this.calculateSectionOffsets();
    window.addEventListener('wheel', this.handleMouseWheel, { passive: false });
    window.addEventListener('touchstart', this.touchStart);
    window.addEventListener('touchmove', this.touchMove);
  },
  unmounted() {
    window.removeEventListener('wheel', this.handleMouseWheel, { passive: false });
    window.removeEventListener('touchstart', this.touchStart);
    window.removeEventListener('touchmove', this.touchMove);
  },
}
</script>

<style>
#app {
  font-family: 'Times New Roman', Times, serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #362e2b;
  text-align: center;
}

#container {
  height: 100%;
  width: 100%;
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
    background-position: 0 75%;
  }

  50% {
    background-position: 100% 75%;
  }

  100% {
    background-position: 0 75%;
  }
}

@keyframes animate2 {
  0% {
    background-position: 100% 75%;
  }

  50% {
    background-position: 75% 0%;
  }

  100% {
    background-position: 100% 75%;
  }
}
</style>
