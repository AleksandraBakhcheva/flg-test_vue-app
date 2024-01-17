<template>
  <div class="card">
    <div class="card-header">
      <h3>{{ headerName }}</h3>
      <img src="../assets/settings-icon.svg" alt="settings-icon" />
    </div>
    <slot name="content"></slot>
  </div>
</template>

<script>
export default {
  name: "CardView",
  props: {
    headerName: String,
  },
};
</script>

<style>
.card {
  width: 450px;
  height: 350px;
  border: 1px solid #000000;
  border-radius: 10px;
}

.card-header {
  display: flex;
  margin: 4%;
  padding-bottom: 2%;
  justify-content: space-between;
  border-bottom: 1px solid #9a9797;
}

.card img {
  width: 25px;
  cursor: pointer;
}
</style>
