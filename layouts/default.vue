<template>
  <div>
    <navbar />
    <div ref="cursor" class="cursor" />
    <nuxt />
  </div>
</template>

<script>
import navbar from '~/components/navbar.vue'
export default {
  components: {
    navbar
  },
  created () {
    onmousemove = this.onmousemove
    onscroll = this.onscroll
    onclick = this.onclick
  },
  methods: {
    onmousemove (e) {
      const cursor = this.$refs.cursor
      cursor.style.left = e.pageX + 'px'
      cursor.style.top = e.pageY + 'px'
      cursor.setAttribute('data-fromTop', (cursor.offsetTop - scrollY))
    },
    onscroll () {
      const fromTop = parseInt(this.$refs.cursor.getAttribute('data-fromTop'))
      this.$refs.cursor.style.top = scrollY + fromTop + 'px'
    },
    onclick () {
      const cursor = this.$refs.cursor
      if (cursor.classList.contains('click')) {
        cursor.classList.remove('click')
      }
    }
  }
}
</script>

<style>
body {
  font-family: 'Inter', sans-serif;
  font-weight: 500;
}

html {
  scroll-behavior: smooth;
}

* {
  box-sizing: border-box;
  z-index: 1;
  cursor: none;
}

img:hover .cursor {
  mix-blend-mode: normal;
}

.cursor {
  position: absolute;
  left: 0;
  top: 0;
  /* border: 1.5px solid white; */
  width: 30px;
  height: 30px;
  border-radius: 50%;
  transform: translate(-50%, -50%);
  mix-blend-mode: difference;
  z-index: 1000000;
  pointer-events: none;
  transition: transform ease-in-out 0.2s;
}
.cursor::after, .cursor::before {
  content: '';
  position: absolute;
  width: 30px;
  height: 30px;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  background-color: white;
  border-radius: 50%;
}
.cursor::before {
  background-color: white;
}
.cursor.click::before{
  animation: click 500ms ease forwards;
}

@keyframes click {
  0% {
    opacity: 1;
    transform: translate(-50%, -50%) scale(1);
  }
  100% {
    opacity: 0;
    transform: translate(-50%, -50%) scale(3);
  }
}
</style>
