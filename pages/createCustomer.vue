<template>
  <div>
    <!-- TODO: -->
    <!-- navbar -->
    <!-- navbar END-->
    <h1>createCustomer</h1>
    <form @submit.prevent="createCustomer">
      <label for="">舊客戶姓名:</label>
      <input type="text" placeholder="舊客戶姓名" />
      <label for="">新客戶姓名:</label>
      <input type="text" placeholder="新客戶姓名" />
      <br />
      <label for="">購買日期: </label>
      <input type="radio" />
      <!--今天或 日曆給它選 -->
      <input type="radio" />
      <br />
      <label for="">購買品項：</label>
      <select name="" id="">
        <option value="">保養品</option>
        <option value="">機器</option>
        <option value="">保健食品</option>
        <option value="">TR90</option>
        <option value="">輔銷品</option>
      </select>
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
      <button>新增客戶資料</button>
    </form>
  </div>
</template>
<script>
export default {
  name: "createCustomer",
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