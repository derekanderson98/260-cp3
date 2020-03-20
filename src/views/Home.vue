<template>
  <div>
    <div class="wrapper">
      <p>Search: </p>
      <div class="search">
        <form class="pure-form">
          <i class="fas fa-search"></i><input v-model="searchText" />
        </form>
      </div>
    </div>
    <AreaList :areas="areas" />
  </div>
</template>

<script>
import AreaList from "../components/AreaList.vue"
export default {
  name: 'Home',
  components: {
    AreaList
  },
  data() {
    return {
      searchText: '',
    }
  },
  computed: {
    areas() {
      return this.$root.$data.areas.filter(area => area.name.toLowerCase().search(this.searchText) >= 0);
    }
  },
}
</script>

<style>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.search {
  border: 1px solid #ccc;
  border-radius: 4px;
  width: 50%;
}

form {
  display: table;
  width: 100%;
}

i {
  display: table-cell;
  padding-left: 10px;
  width: 1px;
}

input {
  display: table-cell;
  font-size: 20px;
  border: none !important;
  box-shadow: none !important;
  width: 100%;
  height: 40px;
}
</style>
