<template>
  <div>
    <transition
      enter-class="opacity-0"
      enter-to-class="opacity-100 duration-1000"
    >
      <img
        class="object-center mx-auto h-64 w-auto"
        :src="choiceImage"
        @click="randomImage(images)"
        alt="クリックすると画像変わるよ！"
      />
    </transition>
    <a class="myName">Kiichi Hamanaka</a>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        require('~/assets/images/bug.png'),
        require('~/assets/images/zikannai.png'),
        require('~/assets/images/kimotti.jpg'),
      ],
      choiceImage: null,
    }
  },
  methods: {
    randomItem(items) {
      return items[Math.floor(Math.random() * items.length)]
    },
    randomImage(items) {
      const tmp = this.choiceImage
      this.choiceImage = this.randomItem(this.images)
      if (tmp === this.choiceImage) this.randomImage(items)
    },
  },
  mounted() {
    this.randomImage(this.images)
  },
}
</script>

<style>
@font-face {
  font-family: 'pop';
  src: url('~assets/fonts/hgp_pop.ttf') format('truetype');
}
.myName {
  font-family: pop;
  font-size: xx-large;
  background-image: linear-gradient(
    to left,
    violet,
    indigo,
    blue,
    green,
    yellow,
    orange,
    red
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
