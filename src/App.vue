<template>
  <div id="app" class="demo">
    <div id="demo">
      <form id="search">
        Search <input name="query" v-model="searchQuery" />
      </form>
      <GridList
        :heroes="gridData"
        :columns="gridColumns"
        :filter-key="searchQuery"
      >
      </GridList>
    </div>
  </div>
</template>

<script>
import GridList from './components/GridList'
export default {
  name: 'app',
  components: {GridList},
  data: function(){
    return {
      searchQuery: "",
      gridColumns: ["name", "power"],
      gridData: [
        { name: "Chuck Norris", power: Infinity },
        { name: "Bruce Lee", power: 9000 },
        { name: "Jackie Chan", power: 7000 },
        { name: "Jet Li", power: 8000 }
      ]
    }
  }
}
</script>

<style>
body {
  font-family: Helvetica Neue, Arial, sans-serif;
  font-size: 14px;
  color: #444;
}
</style>