<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>

        <ion-title class="ion-text-center">Ingresa a tu cuenta</ion-title>
        <img src="@/assets/logo.png" alt="Logo"  style="width: 100%; max-width: 200px; margin: auto; display: block;">
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <ion-item>
        <ion-label position="floating">Correo Electrónico</ion-label>
        <ion-input type="email" v-model="email"></ion-input>
      </ion-item>
      <ion-item>
        <ion-label position="floating">Contraseña</ion-label>
        <ion-input type="password" v-model="password"></ion-input>
      </ion-item>
      <ion-text class="ion-text-center">
        <router-link to="/forgot-password">¿Olvidaste tu contraseña?</router-link>
      </ion-text>
      <ion-button size="short" expand="block" @click="login">Iniciar Sesión</ion-button>
    
    </ion-content>
  </ion-page>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    login() {
      // Aquí puedes agregar la lógica para iniciar sesión, por ejemplo, enviar los datos a un servidor
      console.log('Correo Electrónico:', this.email);
      console.log('Contraseña:', this.password);
    }
  }
}
</script>