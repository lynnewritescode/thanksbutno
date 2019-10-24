<template>
  <div class="logo">
    <h1 class="title">
      thanks! <br />but no.
    </h1>
    <h2 class="subtitle">
      An app to help you say no to requests.
    </h2>
  </div>
</template>

<style lang="scss">
.title {
  transform: matrix(1, -0.1, 0, 1, 0, 0);
  -ms-transform: matrix(1, -0.1, 0, 1, 0, 0);
  -webkit-transform: matrix(1, -0.1, 0, 1, 0, 0);
  font-family: "Oswald", Sans-serif;
  text-transform: uppercase;
  font-weight: 400;
  font-size: 56px;
  line-height: 1.2;
  margin: 0 0 10px;
  // font-size: 70px;
  text-shadow: 4px 5px #e6e6d8, 6px 7px #c6a39a;
}

.subtitle {
  font-weight: 300;
  font-size: 20px;
  color: #333333;
  word-spacing: 5px;
  margin-bottom: 15px;
  transform: matrix(1, -0.1, 0, 1, 0, 0);
  -ms-transform: matrix(1, -0.1, 0, 1, 0, 0);
  -webkit-transform: matrix(1, -0.1, 0, 1, 0, 0);
}

@media (min-width: 600px) {
  .title {
    br {
      display: none;
    }
  }
}
</style>