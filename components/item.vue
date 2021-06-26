<template>
    <div class="container">
      <div class="icon">
        <img v-if="logo" src="/favicon.ico" class="logo">
        <img v-else src="/item.png" class="item">
      </div>
      <div class="content">
        <h1 class="title">{{title}}</h1>
        <h3 class="sub">{{sub}}</h3>
      </div>
    </div>
</template>

<script>
    export default {
        name: "item",
        props:['title','sub','logo']
    }
</script>

<style scoped>
  .container{
    padding: 0 0 0 20px;
    width: 100%;
    height: 65px;
    display: flex;
    transition: all 0.3s;
  }
  .icon{
    padding: 10px;
    display: flex;
    align-content: center;
    height: 100%;
  }
  .icon .logo {
    width: 40px;
    height: 40px;
    padding: 3px;
    border-radius: 7px;
    background-color: rgba(255, 165, 0, 0.2);

  }
  .icon .item{
    width: 25px;
    height: 25px;
    padding: 3px;
  }
  .content{
    padding-left: 10px;

    display: flex;
    align-content: center;
    flex-wrap: wrap;
  }
  .title{
    width: 100%;
    font-family: 'IBM Plex Sans', sans-serif;
    color: white;
    font-size: 12pt;
    font-weight: 500;
  }
  .sub{
    width: 100%;
    font-size: 10pt;
    color: gray;
    margin-top: 3px;
    font-weight: 100;
    font-family: 'IBM Plex Sans', sans-serif;
  }
  .container:hover{
    cursor: pointer;

    background-color: rgba(12, 12, 12, 0.35);
  }

</style>
