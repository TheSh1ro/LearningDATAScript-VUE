<script>
export default {
  data() {
    return {
      services: [
        {
          name: "João Fária",
          desc: "Conserto telhados",
          email: "joao123@gmail.com",
          contact: "996587412",
        },
        {
          name: "Gabriel Mecânico",
          desc: "Conserto carros",
          email: "gabriel123@gmail.com",
          contact: "276587412",
        },
        {
          name: "Roberto Pedrosa",
          desc: "Conserto carros",
          email: "Roberto123@gmail.com",
          contact: "276587412",
        },
        {
          name: "Antonia da Rosa",
          desc: "Pinto casas",
          email: "Antonia3333@gmail.com",
          contact: "276587412",
        },
        {
          name: "Marcelo Silva",
          desc: "Conserto carros",
          email: "Roberto123@gmail.com",
          contact: "276587412",
        },
        {
          name: "Fábio Alcantra",
          desc: "Conserto carros",
          email: "Roberto123@gmail.com",
          contact: "276587412",
        },
        {
          name: "João Fária",
          desc: "Conserto telhados",
          email: "joao123@gmail.com",
          contact: "996587412",
        },
        {
          name: "Gabriel Mecânico",
          desc: "Conserto carros",
          email: "gabriel123@gmail.com",
          contact: "276587412",
        },
        {
          name: "Roberto Pedrosa",
          desc: "Conserto carros",
          email: "Roberto123@gmail.com",
          contact: "276587412",
        },
        {
          name: "Antonia da Rosa",
          desc: "Pinto casas",
          email: "Antonia3333@gmail.com",
          contact: "276587412",
        },
        {
          name: "Fábio Alcantra",
          desc: "Conserto carros",
          email: "Roberto123@gmail.com",
          contact: "276587412",
        },
        {
          name: "João Fária",
          desc: "Conserto telhados",
          email: "joao123@gmail.com",
          contact: "996587412",
        },
        {
          name: "Gabriel Mecânico",
          desc: "Conserto carros",
          email: "gabriel123@gmail.com",
          contact: "276587412",
        },
        {
          name: "Roberto Pedrosa",
          desc: "Conserto carros",
          email: "Roberto123@gmail.com",
          contact: "276587412",
        },
        {
          name: "Antonia da Rosa",
          desc: "Pinto casas",
          email: "Antonia3333@gmail.com",
          contact: "276587412",
        },
      ],
    };
  },
  methods: {
    salvar() {
      if (this.newname.length > 2) {
        this.services.push({
          name: this.newname,
          desc: this.newdesc,
          email: this.newemail,
          contact: this.newcontact,
        });
        // Resetando inputs
        this.newname = "";
        this.newdesc = "";
        this.newemail = "";
        this.newcontact = "";
      }
    },
  },
};
</script>

<template>
  <main>
    <div id="welcome">
      <h1>Encontrar prestadores de serviço nunca foi tão fácil</h1>
      <h3>Divulgue também os seus serviços!</h3>
    </div>
    <div id="content">
      <span class="card" v-for="service of services" v-bind:key="service.email">
        <p class="card-name">{{ service.name }}</p>
        <p class="card-desc">{{ service.desc }}</p>
        <p class="card-email">{{ service.email }}</p>
        <p class="card-contact">{{ service.contact }}</p>
      </span>
    </div>
    <div id="form">
      <h1 class="form-title">Divulgue seu serviço</h1>
      <section class="input-block input-info">
        <input
          type="text"
          placeholder="Nome"
          v-model="newname"
          style="font-weight: bolder"
        />
      </section>
      <section class="input-block input-desc">
        <input type="text" placeholder="Descrição" v-model="newdesc" />
      </section>
      <section class="input-block input-info">
        <input type="text" placeholder="Email" v-model="newemail" />
      </section>
      <section class="input-block input-info">
        <input
          type="text"
          placeholder="Número de celular"
          v-model="newcontact"
        />
      </section>
      <button @click="salvar">Divulgar</button>
    </div>
  </main>
</template>
<style scoped>
#main {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #b7c3f2;
}
#welcome {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 46vh;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.4);
}
#welcome > h3 {
  font-weight: normal;
}
#content {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-template-rows: repeat(2, 1fr);
  justify-items: center;
  gap: 50px;
  padding: 50px;
}
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 5px;
  background-color: #7a99f6;
  border: 2px groove black;
  width: 200px;
  height: 200px;
}
.card-name {
  font-size: 1.2rem;
  font-style: normal;
  font-weight: bolder;
}
.card-desc {
  font-size: 1.1rem;
  font-style: italic;
}
.card-email {
  font-size: 1rem;
  font-style: normal;
}
.card-contact {
  font-size: 1rem;
  font-style: normal;
}
#form {
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  height: fit-content;
  width: fit-content;
  gap: 2px;

  padding: 20px;
  background-color: rgba(0, 0, 0, 0.2);
  border-radius: 20px;
}
.form-title {
  font-size: 22px;
  font-weight: normal;
  text-decoration: underline;
}
.input-block {
  display: flex;
  flex-direction: row;
}
.input-block > input {
  text-align: center;
  width: 50vw;
  border-radius: 8px;
  padding: 5px;
}
.input-info {
  min-height: 5vh;
  height: fit-content;
}
.input-desc {
  min-height: 20vh;
  height: fit-content;
}
#form > button {
  padding: 5px;
  font-weight: bolder;
}
</style>
