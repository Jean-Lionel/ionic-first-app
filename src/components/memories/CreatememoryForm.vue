<template>
  <form>
      <ion-list>
          <ion-item>
              <ion-label position="floating"> Title</ion-label>
              <ion-input type="text" name="title"></ion-input>
          </ion-item>
          <ion-item>
              <ion-label position="floating">URL </ion-label>
              <ion-input type="url" name="url"></ion-input>
          </ion-item>
          <ion-item>
              <ion-label position="floating">Description</ion-label>
              <ion-textarea rows="5"></ion-textarea>
          </ion-item>
      </ion-list>
      <ion-button expand="block" class="">Save</ion-button>
  </form>
</template>

<script>
import {IonList, IonButton, IonItem, IonLabel, IonInput, IonTextarea} from "@ionic/vue"
export default {
    components:{
        IonList,
        IonButton,
        IonItem,
        IonLabel,
        IonInput,
        IonTextarea
    }

}
</script>

<style>

</style>