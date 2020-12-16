<template>
  <div>
    <transition
      enter-class="opacity-0"
      enter-to-class="opacity-100 duration-1000"
    >
      <img
        class="object-center mx-auto h-64 w-auto"
        src="~/assets/images/bug.png"
      />
    </transition>
    <a class="myName">Kiichi Hamanaka</a>
  </div>
</template>
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
