<template>
  <div class="container">
    <h1 class="aboutyou">About You</h1>
    <form @submit.prevent="getFormValues">
      <div class="name">
        <lable>First Name</lable>
        <div><input type="text" v-model="login_data.firstname" /></div>
      </div>

      <div class="name">
        <label>Last Name</label>
        <div><input type="text" v-model="login_data.lastname" /></div>
      </div>

      <div class="name">
        <label>Pin Code</label>
        <div><input type="text" v-model="login_data.pincode" /></div>
      </div>

      <div class="submit-button">
        <RouterLink to="/product">
          <button type="submit" v-on:click="login">Submit</button>
        </RouterLink>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  methods: {
    login() {
      //    console.log(this.login_data)

      this.$router.push({
        path: "/product",
        query: this.login_data,
      });
    },
  },

  data() {
    return {
      login_data: {
        firstname: "",
        lastname: "",
        pincode: "",
      },
    };
  },
};
</script>

<style>
.container {
  height: 300px;
  width: 200px;
  background-color: rgb(237, 235, 235);
}
.name {
  margin-top: 10px;
  margin-left: 10px;
}

.submit-button {
  margin-top: 10px;
  margin-left: 40px;
}

.aboutyou {
  margin-left: 10px;
  font-family: Arial, Helvetica, sans-serif;
}
</style>
