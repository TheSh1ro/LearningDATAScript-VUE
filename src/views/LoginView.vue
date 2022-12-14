<script>
export default {
  data() {
    return {
      user: [{ login: "", password: "", email: "" }],
      register: [
        {
          login: "",
          password: "",
          email: "",
          name: "",
          secondname: "",
          age: "",
          number: "",
        },
      ],
    };
  },
};
</script>

<template>
  <main>
    <div class="login-area">
      <h1>Crie sua conta</h1>
      <div class="login-inputs">
        <input type="text" placeholder="Usuário" v-model="this.user.login" />
        <input type="text" placeholder="Senha" v-model="this.user.password" />
        <input type="text" placeholder="Email" v-model="this.user.email" />
        <RouterLink to="/">
          <button>Próximo</button>
        </RouterLink>
      </div>
      <p>Ou então entre utilizando:</p>
      <section class="login-with">
        <span class="login-with-item">Facebook</span>
        <span class="login-with-item">Google</span>
        <span class="login-with-item">Apple</span>
      </section>
    </div>
  </main>
</template>

<style scoped>
#main {
  background-color: #afcbfb;
}
.login-area {
  margin: 5vh;
  padding: 30px 450px;
  cursor: default;

  background-color: #7a99f6;
  border: 5px solid black;
  color: white;
  border-radius: 20px;

  display: flex;
  flex-direction: column;
  text-align: center;
  row-gap: 5px;
  flex-wrap: wrap;
}
input {
  text-align: center;
  color: black;
  padding: 5px;
  border-radius: 10px;
  border: 2px solid black;
}
.login-inputs {
  display: flex;
  flex-direction: column;
  column-gap: 5px;
}
h1 {
  font-size: 1.8rem;
  font-weight: bolder;
}
p {
  font-size: 1.2rem;
  font-weight: bolder;
  color: white;
}
.login-with {
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 5px;
}
.login-with-item {
  cursor: pointer;
  padding: 5px;
  border-radius: 5px;
}
.login-with-item:hover {
  background-color: rgba(0, 0, 0, 0.6);
  color: red;
}
.redirect-cadastro {
  font-size: 12px;
  text-decoration: underline;
  cursor: pointer;
}
.redirect-cadastro:hover {
  color: red;
}
button {
  align-self: center;
  width: fit-content;
  padding: 5px;
  color: black;
  border: 2px solid black;
  border-radius: 5px;
  margin-top: 5px;
}
button:active {
  border-color: yellow;
}
.testing {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: black;
  background-color: rgba(0, 0, 0, 0.6);
  padding: 10px 30px;
}
</style>
