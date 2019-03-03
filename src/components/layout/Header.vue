<template>
  <header class="header">
    <div id="brand">
      <img id="logo" alt="Vue logo" src="../../assets/logo.png">
    </div>
    <div id="title">
      <h1>
        <span id="vue">VUE</span> Todo
      </h1>
      <div id="nav">
        <router-link to="/">Home</router-link>|
        <router-link to="/about">About</router-link>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
.header {
  background: #f2f3f4;
  color: #333;
  text-align: center;
  padding: 10px;
  display: flex;
}

#brand {
  flex: 4;
}

#logo {
  max-height: 100px;
}

#title {
  flex: 6;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

#vue {
  color: MEDIUMSEAGREEN;
}

#nav {
  padding: 10px;
}

a {
  color: #333;
  text-decoration: none;
  letter-spacing: 1px;
  margin-right: 5px;
}

a:hover {
  color: MEDIUMSEAGREEN;
}
</style>


