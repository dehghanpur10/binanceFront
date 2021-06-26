<template>
  <div class="container">
    <div class="logo">
      <img src="/logo.png">
    </div>
    <more></more>
    <option-menu :data="data[0]" title="Buy Crypto" :sub="true"></option-menu>
    <option-menu title="Market" :sub="false"></option-menu>
    <option-menu :data="data[1]" title="Trade" :sub="true"></option-menu>
    <option-menu :data="data[2]" title="Derivatives" :sub="true"></option-menu>
    <option-menu :data="data[3]" title="Finance" :sub="true"></option-menu>
    <option-menu title="NFT" :sub="false"></option-menu>
    <option-menu title="Log In" :sub="false"></option-menu>
    <button class="register">Register</button>
    <option-menu title="Download" :sub="false"></option-menu>
    <option-menu title="English" :sub="false"></option-menu>
    <div>
      <p style="color: white;margin: 0 7px">|</p>
    </div>
    <div>
      <p style="color: white;">USD</p>
    </div>



  </div>
</template>

<script>
  import More from "./more";
  import optionMenu from "../components/optionMenu";


  export default {
    name: "topHeader",
    components: { More,optionMenu},
    data(){
      return{
        data:[
          [{title:'Credit/Debit Card',sub:'Visa, Mastercard'},{title:'P2P Trading',sub:'Bank transfer and 100+ options'},{title:'Third-party Payment',sub:'Simplex, Banxa, Paxos'}]
          ,[{title:'Convert',sub:'The easiest way to trade'},{title:'Classic',sub:'simple and easy-to-use interface'},{title:'Advanced',sub:'Full access to all trading tools'},{title:'Margin',sub:'Increase your profits with leverage'},{title:'P2P',sub:'Bank transfer and 100+ options'},{title:'Stock Token',sub:'Trade Stocks With Crypto'}]
          ,[{title:'Binance Futures Overview',sub:'View our full range of crypto-derivatice instruments'},{title:'USD-M Futures',sub:'Perpetual or Quarterly Contracts Settled in USDT or BUSD'},{title:'COIN-M Futures',sub:'Perpetual or Quarterly Contracts settled in Crypto currency'},{title:'Vanilla Options',sub:'Buy and Sell European style Vanilla Options'},{title:'Leveraged Tokens',sub:'Enjoy increased leverage without risk of liquidation'},{title:'Battle',sub:'Battle to Win. Long vs Short'}]
          ,[{title:'Binance Earn',sub:'One-stop Investment Solution'},{title:'Binance Pool',sub:'Mine more rewards by connecting to the pool'},{title:'Binance Visa Card',sub:'Convert and pay with crypto worldwide'},{title:'Crypto Loans',sub:'Get an instant loan secured by crypto assets'},{title:'Liquid Swap',sub:'Become a liquidity provider & earn double'}]
        ]
      }
    }
  }
</script>

<style scoped>
  .container {
    display: flex;
    justify-content: flex-start;
    align-content: center;
    align-items: center;
    background-color: rgb(18, 22, 28);
    width: 100%;
    height: 75px;
  }

  .logo {
    width: 13%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: center;
  }

  .logo img {
    width: 100%;
    height: auto;
    cursor: pointer;
  }
  .register{
    width: 110px;
    height: 40px;
    background-color: rgb(240 185 11);
    outline: none;
    border:none;
    font-family: 'IBM Plex Sans', sans-serif;
    font-size: 13pt;
    margin-left: 30px;
    border-radius: 5px;
    transition: all 0.3s;
  }
  .register:hover{
    background-color: #e89f23;
    cursor: pointer;


  }




</style>
