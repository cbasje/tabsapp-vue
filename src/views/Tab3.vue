<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-back-button></ion-back-button>
        </ion-buttons>
        <ion-title>Tab 3 + ID {{ id }}</ion-title>
      </ion-toolbar>
      <ion-toolbar>
        <ion-searchbar placeholder="Lid" inputmode="search" type="search" :debounce="250" showCancelButton="250"></ion-searchbar>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 3</ion-title>
        </ion-toolbar>
      </ion-header>
      
      <ExploreContainer name="Tab 3 page" />
    </ion-content>
  </ion-page>
</template>

<script>
import { IonPage, IonHeader, IonToolbar, IonButtons, IonBackButton, IonSearchbar, IonTitle, IonContent } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';
import { defineComponent } from 'vue';
import { useRoute } from 'vue-router';

export default defineComponent({
  name: 'Tab3',
  components: { ExploreContainer, IonHeader, IonToolbar, IonButtons, IonBackButton, IonSearchbar, IonTitle, IonContent, IonPage },
  setup() {
    const route = useRoute();
    const { id } = route.params;
    return { id };
  }
})
</script>