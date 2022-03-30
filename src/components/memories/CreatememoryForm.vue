<template>
  <form class="ion-padding" @submit.prevent="submitForm">
      <ion-list>
          <ion-item>
              <ion-label position="floating"> Title</ion-label>
              <ion-input type="text" required v-model="enteredTitle"></ion-input>
          </ion-item>
          <ion-item>
              <ion-label position="floating">URL </ion-label>
              <ion-input type="url" required="required" v-model="enterUrl"></ion-input>
          </ion-item>
          <ion-item>
              <ion-label position="floating">Description</ion-label>
              <ion-textarea rows="5" v-model="enterDescription"></ion-textarea>
          </ion-item>
      </ion-list>
      <ion-button expand="block" type="submit">Save</ion-button>
  </form>
</template>

<script>
import {IonList, IonButton, IonItem, IonLabel, IonInput, IonTextarea} from "@ionic/vue"
export default {
    emits:['save-memory'],
    components:{
        IonList,
        IonButton,
        IonItem,
        IonLabel,
        IonInput,
        IonTextarea
    },
    data() {
        return {
            enteredTitle : '',
            enterUrl : '',
            enterDescription : '',
        }
    },
    methods:{
        submitForm(){
            const memoryData = {
                image: this.enterUrl,
                title: this.enteredTitle,
                body: this.enterDescription,

            }
            
            this.$emit('save-memory', memoryData);
        }
    }

}
</script>

<style>

</style>