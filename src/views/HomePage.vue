<template>
  <Header />
  <main class="container">
    <Card headerName="Общая информация">
      <template #content>
        <div class="card-general">
          <p><span>Имя: </span>Иван</p>
          <p><span>Фамилия: </span> Иванов</p>
          <p><span>Номер профиля: </span>75464567834</p>
          <p><span>Число заказов: </span>300</p>
        </div>
      </template>
    </Card>
    <Card headerName="Аватар">
      <template #content>
        <Avatar />
      </template>
    </Card>
    <Card headerName="Контактная информация">
      <template #content>
        <div class="card-general">
          <p><span>Телефон: </span>+7(900)100-00-00</p>
          <p><span>Email: </span> email@email.com</p>
          <a href="/some-action"><button>Изменить телефон</button></a>
          <a href="/some-action"><button>Изменить email</button></a>
        </div>
      </template>
    </Card>
  </main>
  <Footer />
</template>

<script>
import Header from "../components/Header.vue";
import Card from "../components/Card.vue";
import Avatar from "../components/Avatar.vue";
import Footer from "../components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Card,
    Avatar,
    Footer,
  },
};
</script>

<style scoped>
.container {
  display: flex;
  padding: 3% 5%;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 10px;
}

.card-general {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  padding: 5%;
  gap: 50px;
}

span {
  font-weight: 600;
}

button {
  height: 50px;
}
</style>
