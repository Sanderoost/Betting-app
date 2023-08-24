<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-title>Welcome back</ion-title>
      <ion-img
        src="https://i.redd.it/qc8xc8wnkbuz.jpg"
        class="login-image"
        alt="The Wisconsin State Capitol building in Madison, WI at night"
      ></ion-img>
      <ion-col>
          <ion-item>
            <ion-input label="Username"></ion-input>
          </ion-item>
          <ion-item>
            <ion-input label="Password"></ion-input>
          </ion-item>
        <ion-col>
          <ion-button onclick="login">Log In</ion-button>
          <p>or</p>
          <ion-button>Sign Up</ion-button>
        </ion-col>
      </ion-col>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonRow, IonCol, IonTitle, IonItem, IonInput, IonContent, IonButton } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';
export default {
  name: 'login',
  components: { ExploreContainer },
  setup() {
    return {
      IonPage,
      IonTitle,
      IonRow,
      IonCol,
      IonButton,
      IonItem,
      IonInput,
      IonContent
    }
  },
  methods: {
    login() {
      console.log('login')
    }
  },
}

</script>

<style scoped>
.login-image {
  width: 100%;
  height: 60vh;
  object-fit: cover;
  position: relative;
  &::before{
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 10vh;
    background: linear-gradient(180deg, rgba(0,0,0,0) 0%, rgba(0,0,0,0.5) 100%);
  }
}
</style>