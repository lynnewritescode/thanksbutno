<template>
  <div>
    <header>
      <div class="container">
        <logo />
      </div>
    </header>

    <main>
      <div class="container">
        <h2 class="subtitle">
          An app to help you say no to requests.
        </h2>

        <div class="inputs">
          <div class="input">
            <label for="yourNameInput">Enter your name</label>
            <input
              id="yourNameInput"
              type="text"
              v-model="name"
              value="Enter your name"
            />
          </div>

          <div class="input">
            <label for="recipientNameInput">Enter the recipient's name</label>
            <input
              id="recipientNameInput"
              type="text"
              v-model="recipientName"
              value="Enter the recipient's name"
            />
          </div>
        </div>

        <section class="response">
          <p>
            Hello {{name}},
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Non, laboriosam illum doloremque ducimus impedit autem velit magni quidem eligendi tempore culpa provident esse itaque deleniti, nemo vitae veritatis pariatur! Rerum.
          </p>
          <p>
            Kind regards,<br />
            {{recipientName}}
          </p>
        </section>
      </div>
    </main>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";

export default {
  components: {
    Logo
  },

  data() {
    return {
      name: "",
      recipientName: ""
    };
  }
};
</script>

<style lang="scss">
.container {
  margin: 0 auto;
  max-width: 1400px;
  padding: 0 8%;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.center {
  text-align: center;
}

.inputs {
  display: flex;
  align-items: center;
  margin: 0 0 30px;

  .input {
    margin: 0 20px 0 0;
  }

  label {
    width: 100%;
    font-size: 14px;
    font-weight: 700;
  }

  input {
    width: 100%;
    padding: 8px;
    margin: 5px 0 0;
    display: block;
    min-width: 200px;
  }
}

.response {
  padding: 30px;
  border: 1px solid #666666;
}

p {
  margin: 0 0 15px;
}
</style>
