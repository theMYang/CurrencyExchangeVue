<template>
  <div>
    <el-row :gutter="1">
      <el-col :span="6" v-for="item of CurrencyList" :key="item.currencyId">
        <a href="" class="link-style">
          <div class="grid-content bg-purple">
            <span>
                  {{item.currencyEnName}}
                </span>
            <p>
              {{item.issuePrice}}
            </p>
          </div>
        </a>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'CurrencyShowBlock',
  props: {
    list: Array
  },
  data() {
    return {
      CurrencyList: [{
        "circulationAmount": 0,
        "currencyCode": "101",
        "currencyEnName": "BTC",
        "currencyId": 101,
        "currencyOrder": 0,
        "isShow": 0,
        "issueAmount": 0,
        "issuePrice": 10.000000
      }, {
        "circulationAmount": 0,
        "currencyCode": "102",
        "currencyEnName": "ETH",
        "currencyId": 102,
        "currencyOrder": 0,
        "isShow": 0,
        "issueAmount": 0,
        "issuePrice": 20.000000
      }, {
        "circulationAmount": 0,
        "currencyCode": "103",
        "currencyEnName": "FM",
        "currencyId": 103,
        "currencyOrder": 0,
        "isShow": 0,
        "issueAmount": 0,
        "issuePrice": 30.000000
      }, {
        "circulationAmount": 0,
        "currencyCode": "104",
        "currencyEnName": "MY",
        "currencyId": 104,
        "currencyOrder": 0,
        "isShow": 0,
        "issueAmount": 0,
        "issuePrice": 40.000000
      }]
    }
  }
  }
</script>


<style>
  .el-row {
    margin-bottom: 20px;
    /* &:last-child {
                              margin-bottom: 0;
                            } */
  }
  .el-col {
    border-radius: 4px;
  }
  .bg-purple {
    background: #122331;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 130px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
  .link-style {
    color: #9EB5CA;
    text-decoration: none;
  }
</style>
