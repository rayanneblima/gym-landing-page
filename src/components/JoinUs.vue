<template>
  <section class="join-us">
    <div class="left-join-us">
      <hr />
      <p>
        <span class="stroke-text">Ready to</span>
        <span> level up</span>
      </p>

      <p>
        <span>your body</span>
        <span class="stroke-text"> with us?</span>
      </p>
    </div>

    <div class="right-join-us">
      <form class="email-form" ref="form" @submit.prevent="sendEmail">
        <input
          type="email"
          name="user_email"
          placeholder="Enter your e-mail address here"
          :disabled="mustDisableEmailField"
          required
        />

        <button type="submit" class="btn">
          Join now
        </button>
      </form>
    </div>
  </section>
</template>

<script>
import { defineComponent, ref } from "vue";
import emailjs from 'emailjs-com';

export default defineComponent({
  name: 'JoinUsSection',

  setup () {
    const form = ref(null);
    const mustDisableEmailField = ref(false);

    const sendEmail = () => {
      emailjs.sendForm('service_jekgvx1', 'template_uv3liai', form.value,
      'user_wlzu1KQ4lelekgwxR8bEW')
      .then((result) => {
        console.log(result.text);
        alert(result.text);
        mustDisableEmailField.value = true;
      }, (error) => {
        console.log(error.text);
      })
    };

    return {
      form,
      sendEmail,
      mustDisableEmailField,
    }
  }
})
</script>

<style scoped>
.join-us {
  display: flex;
  gap: 10rem;
  padding: 0 2rem;
}

.left-join-us {
  color: #fff;
  font-size: 3rem;
  font-weight: bold;
  position: relative;
  text-transform: uppercase;
}

.left-join-us > hr {
  border: 2px solid var(--orange);
  border-radius: 20%;
  margin: -10px 0;
  position: absolute;
  width: 10.5rem;
}

.left-join-us > p {
  display: flex;
  gap: 1rem;
  margin: 0;
}

.right-join-us {
  align-items: center;
  display: flex;
  justify-content: center;
}

.email-form {
  background-color: gray;
  display: flex;
  gap: 3rem;
  padding: 1rem 2rem;
}

.email-form > input {
  background-color: transparent;
  border: none;
  color: var(--lightgray);
  outline: none;
}

::placeholder {
  color: var(--lightgray);
}

.email-form > input:disabled {
  cursor: not-allowed;
}

.email-form > button {
  background-color: var(--orange);
  color: #fff;
}
</style>