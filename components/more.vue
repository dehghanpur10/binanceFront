<template>
  <div @mouseenter="showFunction(true)" @mouseleave="showFunction(false)" class="wrap">
    <div class="more">
      <div class="row">
        <div class="col" :class="{'hover':show}"></div>
        <div class="col" :class="{'hover':show}"></div>
        <div class="col" :class="{'hover':show}"></div>
      </div>
      <div class="row">
        <div class="col" :class="{'hover':show}"></div>
        <div class="col" :class="{'hover':show}"></div>
        <div class="col" :class="{'hover':show}"></div>
      </div>
      <div class="row">
        <div class="col" :class="{'hover':show}"></div>
        <div class="col" :class="{'hover':show}"></div>
        <div class="col" :class="{'hover':show}"></div>
      </div>

    </div>
    <div class="content" v-if="display">
      <item v-for="i in data" :title="i.title" :sub="i.sub" :key="i.title" :logo="true"></item>

    </div>
  </div>
</template>

<script>
  export default {
    name: "more",
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
        data: [
          {title: 'Exchange', sub: 'Blockchain and crypto asset exchange'},
          {title: 'Academy', sub: 'Blockchain and crypto education'},
          {title: 'Broker', sub: 'Trading terminal solutions'},
          {title: 'Charity', sub: 'Charity'},
          {title: 'Cloud', sub: 'Enterprise exchange solutions'},
          {title: 'DEX', sub: 'Fast and secure decentralize digital asset'},
          {title: 'Labs', sub: 'Incubator for top blockchain projects'},
          {title: 'Lunchpad', sub: 'Token lunch platform'},
          {title: 'Research', sub: 'Blockchain and crypto asset exchange'},
        ]
      }
    }
  }
</script>

<style scoped>
  .wrap {
    position: relative;

    height: 100%;
    display: flex;
    justify-content: center;
    align-content: center;
    align-items: center;
  }

  .more {
    position: relative;
    padding: 2px;
    width: 25px;
    height: 25px;
    display: flex;
    align-content: space-between;
    flex-wrap: wrap;
  }

  .row {
    width: 100%;
    height: 5px;
    display: flex;
    justify-content: space-between;
  }

  .col {
    cursor: pointer;
    transition: all 0.3s;
    width: 5px;
    height: 100%;
    background-color: #F5F5F5;
  }

  .hover {
    background-color: rgb(240 185 11);
  }

  .content {
    position: absolute;
    top: 75px;
    left: 0;
    width: 360px;
    background-color: rgb(27, 34, 41);
    box-shadow: 0px 0px 5px #292929;
    border-bottom-left-radius: 3px;
    border-bottom-right-radius: 3px;
  }

</style>
