# Flickity for Vue.js

[![npm](https://img.shields.io/npm/v/flickity-vue.svg?style=flat-square)](https://www.npmjs.com/package/flickity-vue)
[![npm](https://img.shields.io/npm/dt/flickity-vue.svg?style=flat-square)](https://www.npmjs.com/package/flickity-vue)

A Vue Component for Flickity.js.
Forked from [vue-flickity](https://github.com/drewjbartlett/vue-flickity) to use a native ES6 static import for compatibility with [Vite](https://vitejs.dev/)

<p align="center">
    <img width="200" src="https://flickity.metafizzy.co/img/flickity-illustration.png" alt="Flickity">
    <img width="200" src="https://vuejs.org/images/logo.png" alt="Vue.js">
</p>

## Installation and usage

See official documentation [here](http://flickity.metafizzy.co/).

  $ npm install flickity-vue

```js
import FlickitySlider from 'flickity-vue';

new Vue({
  components: {
    FlickitySlider
  },
  
  data() {
    return {
      flickityOptions: {
        initialIndex: 3,
        prevNextButtons: false,
        pageDots: false,
        wrapAround: true
        
        // any options from Flickity can be used
      }
    }
  },
  
  methods: {
    next() {
      this.$refs.flickity.next();
    },
    
    previous() {
      this.$refs.flickity.previous();
    }
  }
});
```

```html
<FlickitySlider ref="flickity" :options="flickityOptions">
  <div class="carousel-cell">1</div>
  <div class="carousel-cell">2</div>
  <div class="carousel-cell">3</div>
  <div class="carousel-cell">4</div>
  <div class="carousel-cell">5</div>
</FlickitySlider>

<!-- if you don't want to use the buttons Flickity provides -->
<button @click="previous()">Custom Previous Button</button>
<button @click="next()">Custom Next Button</button>
```
