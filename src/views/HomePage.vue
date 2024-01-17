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
        <div>
          <svg viewBox="0 60 320 320">
            <defs>
              <circle id="circle-clip" cx="50%" cy="50%" r="25%" />
              <clipPath id="avatar-clip">
                <use href="#circle-clip" />
              </clipPath>
            </defs>
            <circle cx="50%" cy="50%" r="50%" fill="white" fill-opacity="0.75">
              <animate
                attributeName="r"
                values="15%;20%;30%;15%;20%;25%;30%;15%"
                dur="2s"
                repeatCount="indefinite"
              />
            </circle>
            <image
              height="50%"
              width="50%"
              x="25%"
              y="25%"
              href="../assets/avatar.jpg"
              clip-path="url(#avatar-clip)"
            />
          </svg></div
      ></template>
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
import Footer from "../components/Footer.vue";
import Card from "../components/Card.vue";

export default {
  name: "App",
  components: {
    Header,
    Card,
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
