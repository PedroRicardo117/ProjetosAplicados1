<template>
  <q-layout>
    <q-page class="login flex flex-center full-heigth">
      <q-page-container>
        <div>
          <q-card>
            <q-card-section>
              <div class="text-h6">Realizar Login</div>
              <form @submit.prevent="login">
                <q-input v-model="username" label="Usuário">
                  <template v-slot:prepend>
                    <q-icon name="account_circle" />
                  </template>
                </q-input>
                <q-input v-model="password" type="password" label="Senha">
                  <template v-slot:prepend>
                    <q-icon name="lock" />
                  </template>
                </q-input>
                <div class="q-gutter-sm">
                  <q-checkbox v-model="remeber" label="Lembrar-se" />
                </div>
                <q-btn rounded icon="check_circle" color="green" label="Entrar" class="full-width" />
                <p></p>
                <!-- <div class="flex flex-center ">
                  <p>Não tem uma conta?
                    <q-btn color="primary" type="submit" flat>Cadastre-se.</q-btn>
                  </p>
                </div> -->
              </form>
            </q-card-section>
          </q-card>
        </div>
      </q-page-container>
    </q-page>
  </q-layout>
</template>

<style>
</style>

<script>
export default {
  name: 'Login',
  data: () => ({
    username: '',
    password: '',
    remeber: false
  }),
  methods: {
    login () {
      this.$router.push('/')
    }
  }
}
</script>
