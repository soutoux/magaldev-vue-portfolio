<template>
  <div class="Contact">
    <h1>Get In Touch</h1>
    <form ref="form" @submit.prevent="sendEmail">
      <main>
        <input class="input" type="text" name="user_name" placeholder="Name" />
        <input
          class="input"
          type="email"
          name="user_email"
          placeholder="Email"
        />
        <input
          class="input"
          type="text"
          name="user_phone"
          placeholder="Phone"
        />
        <textarea
          class="input"
          name="message"
          cols="30"
          rows="10"
          placeholder="Message"
        ></textarea>
      </main>
      <button class="button input" type="submit">Submit Request</button>
    </form>
  </div>
</template>

<script>
import emailjs from "@emailjs/browser";

export default {
  methods: {
    sendEmail() {
      emailjs
        .sendForm(
          "service_mrtknqc",
          "template_sr3fn68",
          this.$refs.form,
          "Y1pS1pI-5RN_92T5N"
        )
        .then(
          () => {
            this.$refs.form.reset();
          },
          () => {
            this.$refs.form.reset();
            alert("Something went wrong. Please try again later.");
          }
        );
    },
  },
};
</script>
<style>
.Contact {
  padding: 0 2rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
main {
  display: flex;
  flex-direction: column;
}
h1 {
  font-size: 2rem;
  font-style: bold;
  display: flex;
}

.input {
  display: flex;
  align-items: center;
  background-color: #181818;
  color: #ccc;
  padding: 10px;
  margin: 10px;
  border-radius: 4px;
  width: 500px;
  resize: none;
}

.input::-webkit-scrollbar {
  display: none;
}

.button {
  display: flex;
  background-color: #00bd7e33 !important;
  text-align: center;
  font-size: 1rem;
  font-style: bold;
  align-items: center;
  justify-content: center;
  transition: 0.3s;
  border: none;
  cursor: pointer;
}

.button:hover {
  background-color: #00bd7e7c !important;
}

@media (min-width: 1024px) {
  .Contact {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}

@media (max-width: 1000px) {
  .Contact {
    margin-top: 1rem;
  }
}

@media (max-width: 600px) {
  .input {
    width: 300px;
  }
}

@media (max-width: 400px) {
  .input {
    width: 250px;
  }
}
</style>
