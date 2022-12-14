<script setup></script>

<template>
  <header>
    <img src="../assets/logo.png" alt="Logo" />
    <div class="header-navblock">
      <RouterLink
        to="/"
        style="cursor: pointer; font-weight: bolder; font-size: 1.2rem"
        >Reey Job</RouterLink
      >
    </div>
    <div class="header-navblock">
      <RouterLink class="header-navbutton" to="/login"
        >Acessar Conta</RouterLink
      >
    </div>
  </header>
</template>

<style scoped>
#header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding-inline: 10px;
  width: 100vw;

  background-color: #58658f;
  border-bottom: 3px solid black;
}
.header-navblock {
  display: flex;
  gap: 15px;
}
.header-navblock > .header-navbutton {
  border-radius: 5px;
  padding: 5px;
  cursor: pointer;
}
.header-navblock > .header-navbutton:hover {
  background-color: #8894c1;
}
#header > img {
  height: 40px;
}
</style>
