<template>
<div class="wrapper">
  <div>
    <div v-for="area in areas" :key="area.id">
      <div class=area>
        <h1>{{area.name}}</h1>
        <router-link to="/detail">
            <button @click="seeDetail(area)">See Status</button>
        </router-link>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'AreaList',
  props: {
    areas: Array
  },
  methods: {
    seeDetail(area) {
      this.$root.$data.detail = area;
    }
  },
}
</script>

<style>
.area {
    text-align: left;
    padding: .5em;
    margin: .5em;
    border: .25em solid grey;
    border-radius: 1em;
    display: flex;
    justify-content: space-between;
}
</style>