<template>
  <div>
    <h2>Product catalogue page</h2>

    <br />
    <table style="width: 100%">
      <tr>
        <th>Product name</th>
        <th>Product price</th>
      </tr>
      <tr>
        <td>first</td>
        <td>second</td>
      </tr>
      <tr>
        <td>500</td>
        <td>400</td>
      </tr>
    </table>
    First Name : {{ $route.query.firstname }} <br />
    Last Name : {{ $route.query.lastname }} <br />
    Pincode : {{ $route.query.pincode }} <br />

    <div class="submit-button">
      <RouterLink to="/about">
        <button type="submit" v-on:click="login">Submit</button></RouterLink
      >
    </div>
  </div>
</template>
<script>
export default {};
</script>

<style>
th,
td {
  border: 1px solid black;
}
</style>
