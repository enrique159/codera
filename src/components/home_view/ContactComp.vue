<template>
  <div class="container" id="contactme">
    <div class="UIAsset">
      <img src="@/assets/handsMobile.png" alt="" />
    </div>
    <div class="formulario">
      <h2 class="title">Contáctanos!</h2>
      <p class="subtitle">
        ¿Tienes un proyecto en mente? Podemos trabajar juntos para hacerlo real! Solo envíanos un mensaje
        o llámanos!
        <a href="tel:6121049341">+52 (612) 104 9341</a>
        o por <a href="https://wa.link/a1sknx"><i class="bi bi-whatsapp"></i> WhatsApp</a>
      </p>
      <form class="contact-form" v-on:submit.prevent="sendEmail">
        <div class="nameemail">
          <input
            type="text"
            name="name"
            id="user_name"
            v-model="name"
            placeholder="Tu nombre"
          />
          <input
            type="email"
            name="email"
            id="user_email"
            v-model="email"
            placeholder="Correo electrónico"
          />
        </div>
        <div class="message">
          <textarea
            name="message"
            id="message"
            placeholder="Algo que nos quieras decir :)"
            v-model="message"
          ></textarea>
        </div>
        <div class="sending">
          <input type="submit" value="Send" id="send" />
          <span>{{ error }}</span>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      message: "",
      error: "",
      sendOk: false,
    }
  },
  methods: {
    validarForm() {
      if (this.name != "") {
        if (this.email != "") {
          if (this.message != "") {
            return true;
          } else return "Necesitas escribir algo en el mensaje ☹️";
        } else return "Falta un correo electrónico! 🥸";
      } else return "Cómo te llamas? no escribiste tu nombre 🧐";
    },

    sendEmail(e) {
      e.preventDefault();
      let valid = this.validarForm();
      if (valid === true) {
        this.$emailjs
          .send(
            "service_8x9x9x9",
            "template_8x9x9x9",
            {
              name: this.name,
              email: this.email,
              message: this.message,
            },
            "user_8x9x9x9"
          )
          .then(
            (response) => {
              console.log("SUCCESS!", response.status, response.text);
              this.sendOk = true;
              this.name = "";
              this.email = "";
              this.message = "";
            },
            (err) => {
              console.log("FAILED...", err);
              this.error = "Something went wrong, try again later 😔";
            }
          );
      } else {
        this.error = valid;
      }
    },
  }
}
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: row;
  height: 80vh;
  width: 80%;
  max-width: 1210px;
  justify-content: center;
  align-items: center;

  .UIAsset {
    width: 40%;
    padding: 24px;
    img {
      width: 100%;
    }
  }

  .formulario {
    width: 60%;
    .title {
      font-size: 2rem;
      font-weight: 900;
      margin: 4px;
    }
    .subtitle {
      margin: 8px 4px 24px;
      a {
        text-decoration: none;
        transition: 0.3s ease-in-out;
        font-weight: 500;
        color: #6200ff;
        i {
          color: inherit;
        }
        &:hover {
          color: #00b7ff;
          i {
            color: #00b7ff;
          }
        }
      }
    }
    .contact-form {
      display: flex;
      flex-direction: column;
      .nameemail {
        display: flex;
        flex-direction: row;
        #user_name,
        #user_email {
          background-color: #f3f3f3;
          font-size: 1rem;
          padding: 12px 16px;
          border-radius: 12px;
          border: none;
          margin: 4px;
          width: 50%;
        }
      }
      .message {
        display: flex;
        flex-direction: column;
        #message {
          font-size: 1rem;
          background-color: #f3f3f3;
          padding: 12px 16px;
          border-radius: 12px;
          height: 78px;
          border: none;
          margin: 4px;
        }
      }
      .sending {
        display: flex;
        flex-direction: row;
        align-items: center;
        column-gap: 2rem;
        #send {
          transition: 0.3s ease-in-out;
          background-color: #4400ff;
          padding: 8px 24px 6px;
          border-radius: 12px;
          font-size: 1rem;
          font-weight: 700;
          border: none;
          color: white;
          cursor: none;
          margin: 4px;
          width: 128px;
          &:hover {
            background-color: #0077ff;
            box-shadow: 0px 8px 43px -7px rgba(0, 162, 255, 0.68);
          }
        }
      }
    }
  }
}

@media only screen and (max-width: 760px) {
  .container {
    width: 80%;
    height: fit-content;
    flex-direction: column;
    .UIAsset,
    .formulario {
      width: 100%;
    }
  }
}
</style>
