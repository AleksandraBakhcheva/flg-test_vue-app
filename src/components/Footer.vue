<template>
  <footer>
    <div class="footer">
      <h4>{{ activity }}!</h4>
      <button @click="fetchData">Are you bored?</button>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterView",
  data() {
    return {
      activity: "hhjgj",
    };
  },
  methods: {
    fetchData() {
      fetch("https://www.boredapi.com/api/activity", {
        method: "GET",
        headers: {
          "Content-type": "application/json",
        },
      })
        .then((response) => {
          response.json().then((data) => {
            this.activity = data.activity;
          });
        })
        .catch((err) => {
          console.error(err);
        });
    },
  },
};
</script>

<style>
.footer {
  display: flex;
  width: 100%;
  height: 120px;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: #ffffff;
  background-color: #535253;
}

h4 {
  padding: 1%;
  text-align: center;
}

button {
  height: 40px;
  padding: 10px;
  font-size: 1rem;
  border-radius: 10px;
  border-width: 0;
  cursor: pointer;
  transition: all 200ms;
  box-shadow: rgba(25, 25, 25, 0.04) 0 0 1px 0, rgba(0, 0, 0, 0.1) 0 3px 4px 0;
  color: #000000;
  background-color: #f7d966;
}

button:hover {
  transform: scale(1.05);
  background-color: #f7d85b;
}
</style>
