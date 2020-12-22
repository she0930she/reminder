<template>
  <div>
    <h1>customer page</h1>
    <!-- TODO: -->
    <!-- navbar -->
    <!-- navbar END-->
    <button @click="reminder" class="btn btn-secondary">本月提醒</button>
    <br />
    <br />
    <form @submit.prevent="historyCustomer">
      <h3>歷史資料</h3>
      <label for="">客戶姓名</label>
      <input v-model="customerName" type="text" placeholder="客戶姓名" />
      <h4>或</h4>
      <input v-model="customerTel" type="text" placeholder="客戶手機號碼" />
      <!-- <h4>
        或<br />
        使用下拉選單尋找客戶
      </h4> -->
      <!-- <select v-model="historyName" id="">
        <option name="historyName" value="" disabled>請選擇客戶姓名</option>
        <option name="historyName" value="">大雄</option>
        <option name="historyName" value="">靜香</option>
        <option value="">胖虎</option>
      </select> -->
      <button>搜尋</button>
    </form>
    <br />
    <br />
    <button>使用產品搜尋客戶</button>
    <br />
    <br />
    <button @click="newCumstomer">新增客戶資料</button>
    <h3>本月提醒區:</h3>
    <h3>客戶歷史資料區:</h3>
    <p>{{ customerList }}</p>
    <h3>新增客戶資料區:</h3>
    <h3>產品搜尋客戶區:</h3>
  </div>
</template>
<script>
export default {
  name: "customer",
  data() {
    return {
      customerName: "",
      customerTel: "",
      customerList: [],
    };
  },
  methods: {
    reminder() {
      console.log("click");
    },
    newCumstomer() {
      console.log("click");
    },
    historyCustomer() {
      console.log("click");
      const historySearch = {
        // return裡面的customerName{{}} 對上 this.customerName
        // testsgitstatus
        customerName: this.customerName,
        customerTel: this.customerTel,
        createdAt: new Date().getTime(),
      };
      console.log("[historySearch]", historySearch);
      this.customerList.push(historySearch);
    },
  },
};
</script>