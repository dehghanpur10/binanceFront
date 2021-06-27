<template>
  <div class="limit_wrap">
    <div class="input" :class="{'cover':I0}">
      <p>Stop</p>
      <input @focus="input0(true)" @blur="input0(false)" type="text">
      <p>USDT</p>
    </div>
    <div class="input" :class="{'cover':I1}">
      <p>Limit</p>
      <input @focus="input1(true)" @blur="input1(false)" type="text">
      <p>USDT</p>
    </div>
    <div class="input" :class="{'cover':I2}">
      <p>Amount</p>
      <input @focus="input2(true)" @blur="input2(false)" type="text">
      <p>BTC</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: "limit",
    methods: {
      input0(state){
        this.I0 = state;
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
        I0:false,
        I1:false,
        I2:false,
      }
    },

  }
</script>

<style scoped>
  .limit_wrap {
    width: 100%;
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

</style>
