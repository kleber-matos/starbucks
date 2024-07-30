<script setup></script>

<template>
  <header>
    <div>
      <img src="../../assets/logo.png" alt="" />

      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Menu</a></li>
          <li><a href="#">Novidades</a></li>
          <li><a href="#">Contato</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style>
header {
  display: flex;
  justify-content: center;
  height: 20vh;
}

header div {
  /* border: solid; */
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 90vw;
}

header img {
  width: 10vw;
  height: 10vh;
  max-width: 110px;
}

header ul {
  /* border: solid; */
  width: 30vw;
  display: flex;
  justify-content: space-between;
}

header li,
a {
  list-style: none;
  text-decoration: none;
  color: black;
}
</style>
