<template>
    <div @mouseenter="showFunction(true)" @mouseleave="showFunction(false)" class="wrap">
      <h1>{{title}}</h1>
      <img  v-if="sub" src="/more.png" class="more" :class="{'reverse':show}">
      <div class="content" v-if="display && sub">
        <item v-for="i in data" :title="i.title" :sub="i.sub" :key="i.title"></item>

      </div>
    </div>

</template>

<script>
    export default {
        name: "optionMenu",
        props:['title','sub','data'],
      methods: {
        showFunction(state) {
          this.show = state;
          this.display = state

        },
      },
      data() {
        return {
          show: false,
          display: false,

        }
      }
    }
</script>

<style scoped>
  .wrap{
    position: relative;
    margin-left:40px ;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
  }
  h1{
    font-weight: 100;
    color: white;
    font-size: 14pt;
    font-family: 'IBM Plex Sans', sans-serif;
    transition: all 0.3s;
  }
  h1:hover{
    cursor: pointer;
    color: rgb(240 185 11);
  ;
  }
  .more{
    width: 15px;
    height: 15px;
    margin-left: 5px;
    transition: all 0.3s;
  }
  .reverse{
    transform: rotateX(180deg);
  }
  .content {
    position: absolute;
    top: 75px;
    left: 0;
    width: 400px;
    background-color: rgb(27, 34, 41);
    box-shadow: 0px 0px 5px #292929;
    border-bottom-left-radius: 3px;
    border-bottom-right-radius: 3px;
  }

</style>
