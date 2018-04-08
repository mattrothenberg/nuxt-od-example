<template>
  <div>
    <div class="wrap flex items-center justify-center">
      <no-ssr>
        <overdrive :id="id" class="lightbox">
          <div class="flex w-full h-full">
            <figure class="bg-grey-dark"></figure>
            <aside class="bg-white"></aside>
          </div>
        </overdrive>
      </no-ssr>
    </div>
    <div class="mask pin"></div>
  </div>
</template>

<script>
export default {
  computed: {
    id () {
      return `item-${this.$route.params.id}`
    }
  }
}
</script>


<style>
  .wrap {
    height: 100vh;
  }

  .mask {
    position: fixed;
    background: rgba(0, 0, 0, .25);
    width: 100%;
    height: 100%;
    z-index: -1;
  }

  .lightbox {
    width: 70%;
    height: 500px;
  }

  figure {
    flex: 2;
  }

  aside {
    flex: 1;
  }
</style>
