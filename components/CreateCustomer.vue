<template>
  <div>
    <!-- createCustomer -->
    <div class="container">
      <form @submit.prevent="createCustomer">
        <label for="">舊客戶姓名:</label>
        <input type="text" placeholder="舊客戶姓名" />
        <br />
        <!-- TODO:抓到客戶姓名，並儲存在object裡面 -->
        <!-- TODO:考慮是否為"每一個新客戶"設定"新id" 供我們辨認-->
        <label for="">新客戶姓名:</label>
        <input type="text" placeholder="新客戶姓名" />
        <br />
        <label for="">購買日期: </label>
        <input type="radio" value="today" />
        <label for="today">今天</label>
        <!--今天或 日曆給它選 -->
        <br />
        <input type="radio" value="chooseDay" />
        <label for="chooseDay">選擇日期</label>
        <br />
        <!-- TODO:把購買品項的JS寫進這份檔案裡 -->
        <label for="">購買品項：</label>
        <select name="" id="">
          <option value="">保養品</option>
          <option value="">機器</option>
          <option value="">保健食品</option>
          <option value="">TR90</option>
          <option value="">輔銷品</option>
        </select>
        <br />
        <label for="">數量</label>
        <input type="number" />
        <br />
        <button>新增購買品項</button>
        <br />
        <br />
        <label for="">Note</label>
        <input type="text" placeholder="備註" />
        <br />
        <br />
        <!-- TODO:新增客戶名單 -->
        <button>新增客戶資料</button>
      </form>
    </div>
  </div>
</template>
<script>
export default {
  name: "CreateCustomer",
  data() {
    return {};
  },
  methods: {
    createCustomer() {
      console.log("click");
      const newShop = {
        customerName: "",
        shopDate: "",
        shopItem1: "",
        shopItem1N: "",
        note: "",
        createdAt: new Date().getTime(),
      };
      console.log("[newShop]", newShop);
    },
  },
};
</script>