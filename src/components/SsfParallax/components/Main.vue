<template>
  <div class="ssf-parallax parallax-container">
    <div class="parallax-overlay" v-if="hasSlot('overlay-content')">
      <slot name="overlay-content"/>
    </div>
    <div class="parallax" ref="parallaxContainer">
      <img :src="src(image)" @load="loaded++" alt="Parallax image"/>
    </div>
  </div>
</template>

<script>

  import './assets/parallax.min.scss'

  import './assets/jquery.min.js'
  import './assets/parallax.min.js'

  export default {
    name: "SsfParallax",

    props: { image: { type: String, required: true }, power: { default: 2.6 } },

    created() {
      this.loaded = 0;
    },

    data() {
      return { loaded: 0 }
    },

    watch: {
      loaded() {
        if (this.loaded > 0)
          $(this.$refs.parallaxContainer).parallax(this.power)
      }
    },

    methods: {
      hasSlot(name = 'default') {
        return !!this.$slots[name] || !!this.$scopedSlots[name]
      },

      src(image) {
        try {
          return image ? require(`@/assets/img/${image}`) : image
        } catch (e) {
          return image
        }
      },
    }
  }
</script>
