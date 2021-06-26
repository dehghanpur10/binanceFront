<template>
    <div class="container0">
      <div class="container">
        <div class="type">
          <div @click="type = 1" class="item" style="border-bottom-left-radius: 7px;border-top-left-radius: 7px" :class="{'active':type === 1}">Spot</div>
          <div @click="type = 2" class="item" :class="{'active':type === 2}">Cross 3X</div>
          <div @click="type = 3" class="item" style="border-bottom-right-radius: 7px;border-top-right-radius: 7px" :class="{'active':type === 3}">Isolated 10X</div>
        </div>
        <h2 style="width: 100%;color: white;padding-left: 10px">BTC/USDT</h2>
        <div class="detail">
          <div class="block" id="main">
            <p>31,760.55</p>
            <p>$31,760.55</p>
          </div>
          <div class="block" id="change">
            <p>24h Change</p>
            <p>+77.81 +5.6%</p>
          </div>
          <div class="block" >
            <p>24h High</p>
            <p>32,730.00</p>
          </div>
          <div class="block" >
            <p>24h Low</p>
            <p>32,700.00</p>
          </div>
          <div class="block" >
            <p>24h Volume(BTC)</p>
            <p>107,254.20</p>
          </div>
          <div class="block" >
            <p>24h Volume(USDT)</p>
            <p>3,254,126,102.25</p>
          </div>
        </div>
      </div>

    </div>
</template>

<script>
    export default {
        name: "top",
      data(){
          return{
            type:1,
          }
      }
    }
</script>

<style scoped>
  .container0{
    width: 100%;
    margin: 3px;
  }
  .container{
    width: 100%;
    background-color: rgb(30 32 38);
    border-radius: 5px;
  }
  .type{
    width: 100%;
    height: 45px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding-right: 20px;
  }
  .item{
    padding:7px;
    background-color: #343434;
    width: 110px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    cursor: pointer;
    transition: all 0.3s;
  }
  .active{
    background-color: rgba(2500, 165, 0, 0.3);
    color:#e89f23;
  }
  .detail{
    width: 100%;
    height: 75px;
    display: flex;
    justify-content: flex-start;
    margin-top:6px ;
    padding-left: 10px;
  }
  .block{
    height: 100%;
    margin-right: 13px ;
  }
  .block p:first-child{
    font-size: 10pt;
    color: gray;
  }
  .block p:last-child{
    font-size: 12pt;
    color: white;
    margin-top: 10px;
  }

  #main p:first-child{
    font-size: 14pt;
    color: forestgreen;
  }
  #main p:last-child{
    margin-top: 6px;
    font-size: 10pt;
    color: gray;
  }
  #change p:first-child{
    font-size: 10pt;
    color: gray;
  }
  #change p:last-child{
    font-size: 12pt;
    color: forestgreen;
    margin-top: 10px;
  }



</style>
