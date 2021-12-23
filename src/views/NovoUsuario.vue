<template>
  <div class="wrapper">
    <div class="container">
      <h1>Novo usuário</h1>
      <form @submit.prevent.stop="enviarFormulario()">
        <div class="form-group">
          <label for="name">Nome</label>
          <input v-model="usuario.name" type="text" name="name" id="name" class="form-control">
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input v-model="usuario.email" type="text" name="email" id="email" class="form-control">
        </div>
        v-model=text
        <div class="form-group">
          <label for="password">Senha</label>
          <input v-model="usuario.password" type="password" name="password" id="password" class="form-control">
        </div>
        <button type="submit" class="btn btn-success">Salvar</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      usuario: {
        nome: '',
        senha: '',
        email: '',
      }
    }
  },
  methods: {
    enviarFormulario() {
      console.log(this.usuario)
    }
  }
}
</script>