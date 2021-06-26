<template>
  <div class="container0">
    <div class="container">
    <div class="header">
      <h1>Place Older</h1>
      <div class="more" @mouseenter="showFunction(true)" @mouseleave="showFunction(false)">
        <div class="circle" :class="{'hover':show}"></div>
        <div class="circle" :class="{'hover':show}"></div>
        <div class="circle" :class="{'hover':show}"></div>


        <div v-if="show" class="moreOption">
          <h3>Trading Rules</h3>
          <h3>FAQ</h3>
          <h3>Spot Tutorial</h3>
        </div>
      </div>
    </div>
    <div class="section">
      <div @click="buy=true" style="border-bottom-left-radius: 7px;border-top-left-radius: 7px;"
           :class="{'option':true,'buy':buy,'deActive':!buy}">BUY
      </div>
      <div @click="buy=false" style="border-bottom-right-radius: 7px;border-top-right-radius: 7px"
           :class="{'option':true,'sell':!buy,'deActive':buy}"> SELL
      </div>
    </div>
    <div class="wallet">
      <img src="/wallet.png">
      <p> - {{type}}</p>
    </div>
    <div class="input" :class="{'cover':I1}">
      <p>Price</p>
      <input @focus="input1(true)" @blur="input1(false)" type="text">
      <p>USDT</p>
    </div>
    <div class="input" :class="{'cover':I2}">
      <p>Amount</p>
      <input @focus="input2(true)" @blur="input2(false)" type="text">
      <p>BTC</p>
    </div>
    <div class="action">
      <p><span>LogIn</span> or <span>Register Now</span></p>
    </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "trade",
    methods: {
      showFunction(state) {
        this.show = state;
        this.display = state;


      },
      input1(state){
        this.I1 = state;
      },
      input2(state){
        this.I2 = state;
      }
    },
    data() {
      return {
        show: false,
        display: false,
        buy: true,
        type: "USDT",
        I1:false,
        I2:false
      }
    },
    watch: {
      buy: function (value) {
        if (value) {
          this.type = 'USDT'
        } else {
          this.type = 'BTC'
        }
      }
    }
  }
</script>

<style scoped>
  .container0{
    width: 100%;
    height: 400px;
    border-radius: 5px;
    margin: 3px;
  }
  .container {
    border-radius: 5px;
    background-color: rgb(30 32 38);
    width: 100%;
    height: 400px;
    padding: 10px;
    display: flex;
    align-content: flex-start;
    flex-wrap: wrap;
  }

  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    align-content: center;
    padding: 0 10px;
    width: 100%;
    height: 40px;
  }

  .header h1 {

    font-size: 13pt;
    color: white;
  }

  .more {
    cursor: pointer;
    display: flex;
    flex-wrap: wrap;
    width: 9px;
    height: 100%;
    align-items: center;
    align-content: center;
    position: relative;
  }

  .moreOption {
    width: 165px;
    background-color: rgb(43 49 57);
    border-radius: 5px;
    position: absolute;
    top: 40px;
    right: 0;

  }

  .moreOption h3 {
    cursor: pointer;
    color: white;
    font-weight: 100;
    padding: 10px;
  }

  .moreOption h3:hover {
    background-color: rgba(40, 40, 40, 0.64);
  }

  .circle {
    width: 4px;
    height: 4px;
    border-radius: 50%;
    margin: 2px;
    background-color: #F5F5F5;
  }

  .hover {
    cursor: pointer;
    background-color: #e89f23;
  }

  .buy {
    background-color: forestgreen;
  }

  .sell {
    background-color: red;
  }

  .deActive {
    background-color: #303030;

  }

  .section {
    cursor: pointer;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 50px;
    margin-top: 20px;
    border-radius: 7px;

  }


  .option {
    width: 150px;
    color: white;
    padding: 12px;
    display: flex;
    justify-content: center;
    align-items: center;


  }

  .wallet {
    margin-top: 10px;
    padding-left: 20px;
    display: flex;
    justify-content: flex-start;
    align-items: center;
  }

  .wallet img {
    width: 30px;
  }

  .wallet p {
    color: white;
  }
  .input{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 40px;
    margin-top: 25px;
    padding: 5px;
    background-color: #303030;
    border-radius: 5px;
  }
  .input input{
    width: 100%;
    height: 80%;
    background-color: rgba(0,0,0,0);
    outline: none;
    border: none;
    color: #F5F5F5;
    direction: rtl;
    font-size: 14pt;

  }
  .input p{
    font-size: 14pt;

    padding: 5px;
    color: #7F828B;
  }
  .cover{
    border: 1px solid #e89f23;
  }
  .action{
    width: 80%;
    height: 40px;
    padding: 15px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #303030;
    margin: 50px auto;
    border-radius: 7px;
  }
  .action p{
    color: white;
    font-size: 14pt;

  }
  .action p span{
    color: #e89f23;
  }
  .action p span:hover{
    cursor: pointer;
  }

</style>
