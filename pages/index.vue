<template>
  <div>
    <header>
      <div class="container center">
        <logo />
      </div>
    </header>

    <main>
      <div class="container">
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

        <div class="center">
          <button class="copyBtn">Copy response!</button>
        </div>
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
@import url(https://fonts.googleapis.com/css?family=Oswald:400|Open+Sans:700);

.container {
  margin: 0 auto;
  max-width: 1400px;
  padding: 0 8%;
}

header {
  padding: 30px 0;
}

.center {
  text-align: center;
}

.inputs {
  margin: 0 0 30px;

  .input {
    width: 100%;
    margin: 0 0 15px;
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

    &:focus {
      border: 2px solid #00dfff;
    }
  }
}

main {
  padding: 0 0 80px;
}

.response {
  padding: 30px;
  max-width: 635px;
  margin: 0 auto 30px;
  border: 1px solid #666666;
}

p {
  margin: 0 0 15px;
}

.copyBtn {
  appearance: none;
  -webkit-appearance: none;
  border: none;
  font-family: inherit;
  font-size: inherit;
  cursor: pointer;
  width: 100%;
  padding: 25px 45px;
  display: inline-block;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: 700;
  outline: none;
  position: relative;
  background: #cb4e4e;
  color: #fff;
  box-shadow: 0 6px #ab3c3c;
  -webkit-transition: none;
  -moz-transition: none;
  transition: none;

  &:after {
    content: "";
    position: absolute;
    z-index: -1;
    -webkit-transition: all 0.3s;
    -moz-transition: all 0.3s;
    transition: all 0.3s;
  }

  &:hover {
    box-shadow: 0 4px #ab3c3c;
    top: 2px;
  }

  &:focus {
    border: 2px solid #00dfff;
    box-shadow: 0 4px #00dfff;
  }
}

@media (min-width: 700px) {
  .inputs {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 -20px 30px;

    .input {
      margin: 0 20px 0;
    }
  }

  .copyBtn {
    width: auto;
  }
}

@media (min-width: 900px) {
  header {
    padding: 40px 0 50px;
  }

  .inputs {
    .input {
      width: auto;
      min-width: 300px;
    }
  }

  .response {
    margin: 0 auto 40px;
  }
}
</style>
