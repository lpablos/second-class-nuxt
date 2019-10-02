<template>
  <div class="error-page">
    <h1>Oops, Ha ocurrido un error</h1>
    <p>Volver a inicio de manera <a href="/">segura</a>!</p>
  </div>
</template>

<style scoped>
.error-page {
  text-align: center;
}

.error-page a {
  text-decoration: none;
  color: red;
}

.error-page a:hover,
.error-page a:active {
  color: salmon;
}
</style>