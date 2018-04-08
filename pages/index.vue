<template>
  <section class="p-8">
    <div class="flex flex-wrap -mx-2">
      <div class="w-full md:w-1/4 px-2 mb-4" v-for="(item, index) in Array(10)" :key="index">
        <no-ssr>
          <overdrive :id="`item-${index}`">
            <nuxt-link :to="index.toString()">
              <div class="bg-grey-light square mx-auto"></div>
            </nuxt-link>
          </overdrive>
        </no-ssr>
      </div>
    </div>
  </section>
</template>

<script>

export default {
}
</script>

<style>
  .square {
    height: 150px;
    width: 150px;
  }
</style>
