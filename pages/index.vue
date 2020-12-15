<template>
  <div class="container">
    <div>
      <Logo />
      <div class="links">
        <a
          href="https://twitter.com/DevuKiichi"
          class="bg-blue-500 font-medium text-white w-1/4 py-2 px-4 mx-1 rounded hover:opacity-75"
        >
          Twitter
        </a>
        <a
          href="https://github.com/KiichiHamanaka"
          class="bg-black font-medium text-white w-1/4 py-2 px-4 mx-1 rounded hover:opacity-75"
        >
          GitHub
        </a>
        <a
          href="https://qiita.com/Kiichi_Hamanaka"
          class="bg-green-500 font-medium text-white w-1/4 py-2 px-4 mx-1 rounded hover:opacity-75"
        >
          Qiita
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
</style>
