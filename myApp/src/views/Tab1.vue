<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Vagas</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">

    
      <ExploreContainer  />
      
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';

export default  {
  name: 'Tab1',
  components: { ExploreContainer, IonHeader, IonToolbar, IonTitle, IonContent, IonPage }
}
</script>
<style scoped>
.head {
  background-color: green;
}
</style>