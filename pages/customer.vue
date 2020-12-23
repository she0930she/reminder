<template>
  <div>
    <div class="container">
      <!-- TODO: -->
      <!-- navbar -->
      <NavBar />
      <!-- navbar END-->
      <h1>customer page</h1>
      <br />

      <div class="customerDiv">
        <div class="remindDiv">
          <button @click="reminder" class="btn reminderBtn">本月提醒</button>
          <Remind />
        </div>
        <br />
        <br />
        <!-- 歷史資料 -->
        <div class="historyDiv">
          <h3>歷史資料</h3>
          <form @submit.prevent="historyCustomer">
            <label for="">客戶姓名</label>
            <input v-model="customerName" type="text" placeholder="客戶姓名" />
            <h4>或</h4>
            <input
              v-model="customerTel"
              type="text"
              placeholder="客戶手機號碼"
            />

            <button>搜尋</button>
          </form>
          <br />
          <br />
          <button>使用產品搜尋客戶</button>
        </div>
        <!-- 歷史資料 END-->
        <!-- 新增客戶資料 -->
        <div class="createDiv">
          <button @click="newCumstomer">新增客戶資料</button>
          <CreateCustomer />
          <!-- <nuxt-link to="createCustomer"
            ><button @click="newCumstomer">新增客戶資料</button>
            </nuxt-link> -->
        </div>
        <!-- 新增客戶資料 END-->
      </div>
      <br />
      <h3>本月提醒區:</h3>
      <h3>客戶歷史資料區:</h3>
      <p>{{ customerList }}</p>
      <div
        v-for="historySearch in customerList"
        :key="historySearch.createdAt"
        class="renderCustomer"
      >
        <div class="customerName">{{ historySearch.customerName }}</div>
        <div class="customerTel">{{ historySearch.customerTel }}</div>
      </div>
      <h3>新增客戶資料區:</h3>
      <h3>產品搜尋客戶區:</h3>
    </div>
  </div>
</template>
<script>
// import NavBar from "@/components/NavBar";
export default {
  name: "customerPage",
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