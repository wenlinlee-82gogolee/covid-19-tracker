<template>
  <div class="grid md:grid-cols-2 gap-4">
    <!-- Box1 -->
    <div class="shadow-md bg-amber-50 p-10 text-center rounded">
      <h3 class="text-3xl text-cyan-900 font-bold mb-5">Cases</h3>
      <div class="text-2xl mb-3">
        <span class="font-bold">New:</span>
        {{ numberWithCommas(stats.NewConfirmed) }}
      </div>
      <div class="text-2xl mb-3">
        <span class="font-bold">Total:</span>
        {{ numberWithCommas(stats.TotalConfirmed) }}
      </div>
    </div>
    <!-- Box2 -->
    <div class="shadow-md bg-amber-100 p-10 text-center rounded">
      <h3 class="text-3xl text-cyan-900 font-bold mb-5">Deaths</h3>
      <div class="text-2xl mb-3">
        <span class="font-bold">New:</span>
        {{ numberWithCommas(stats.NewDeaths) }}
      </div>
      <div class="text-2xl mb-3">
        <span class="font-bold">Total:</span>
        {{ numberWithCommas(stats.TotalDeaths) }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DataBoxes',
  props: ['stats'],
  methods: {
    numberWithCommas(x) {
      return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',');
    },
  },
};
</script>

<style></style>
