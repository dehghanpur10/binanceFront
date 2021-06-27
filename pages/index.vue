<template>
  <div class="container">
    <div class="info">
      <info></info>
      <div class="main">
        <div class="chart"></div>
        <div class="book"></div>
      </div>
    </div>
    <div class="trade">
      <trade></trade>
    </div>


  </div>

</template>

<script>
  import optionMenu from "../components/optionMenu";
  import Trade from "../components/trade";
  import Info from "../components/info";

  export default {
    name: "index",
    components: {Info, Trade, optionMenu}
  }
</script>

<style scoped>
  .container{
    overflow: hidden;
    max-width: 100%;
    height: 1000px;
    background-color: rgb(24 26 32);
    display: flex;
    z-index: 1;

  }
  .trade{
    width: 24%;
  }
  .info{
    width: 76%;
  }
  .main{
    width: 100%;
  }

</style>
