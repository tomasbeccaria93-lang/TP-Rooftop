<template>
  <section class="contacto">
    <h2>Solicitá información</h2>

    <form @submit.prevent="enviarFormulario">
        <p class="descripcion">Completá el formaluraio para poder ponernos en contacto con vos.</p>
        <label>
            Nombre:
            <input type="text" v-model="nombre" required />
        </label>

        <label>
            Email:
            <input type="email" v-model="email" required />
        </label>

        <label>
            Mensaje:
            <textarea v-model="mensaje" required></textarea>
        </label>

        <button type="submit">Enviar</button>
    </form>

    <p v-if="enviado" class="mensaje-ok">
      ¡Mensaje enviado correctamente!
    </p>
  </section>
</template>

<script>
export default {
  data() {
    return {
      nombre: '',
      email: '',
      mensaje: '',
      enviado: false
    }
  },
  methods: {
    enviarFormulario() {
      this.enviado = true
      this.nombre = ''
      this.email = ''
      this.mensaje = ''
    }
  }
}
</script>

<style scoped>
.contacto {
  padding: 30px;
  background-color: #f2f2f2;
}

.contacto h2 {
  text-align: center;
  margin-bottom: 20px;
}

form {
  max-width: 400px;
  margin: auto;
  display: flex;
  flex-direction: column;
}

label {
  margin-bottom: 15px;
}

input,
textarea {
  width: 100%;
  padding: 8px;
  margin-top: 5px;
}

button {
  padding: 10px;
  cursor: pointer;
  width: 418px;
}

.mensaje-ok {
  text-align: center;
  margin-top: 15px;
  color: green;
}
.descripcion{
    text-align: center;
    margin-bottom: 15px;
}
</style>
