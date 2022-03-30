<template>
  <form class="ion-padding" @submit.prevent="submitForm">
      <ion-list>
          <ion-item>
              <ion-label position="floating"> Title</ion-label>
              <ion-input type="text" required v-model="enteredTitle"></ion-input>
          </ion-item>
          <ion-item>
             <ion-thumbnail slot="start">
                 <img :src="previewUrl" alt="">
             </ion-thumbnail>
             <ion-button fill="clear" type="button" @click="takePhoto">
                 <ion-icon slot="start" :icon="camera"></ion-icon>
                 Take a Photo
             </ion-button>
             
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
import {IonList, IonButton, IonItem, IonLabel, IonInput, IonTextarea, IonThumbnail, IonIcon} from "@ionic/vue"
import {camera} from  "ionicons/icons";
import {Plugins , CameraResultType, CameraSource} from "@capacitor/core";

const {Camera} = Plugins;

export default {
    emits:['save-memory'],
    components:{
        IonList,
        IonButton,
        IonItem,
        IonLabel,
        IonInput,
        IonTextarea,
        IonThumbnail,
        IonIcon
    },
    data() {
        return {
            enteredTitle : '',
            enterUrl : '',
            enterDescription : '',
            previewUrl: null,
            camera
        }
    },
    methods:{
        async takePhoto(){
           const photo = await Camera.getPhoto({
               resultType : CameraResultType.Uri,
               source : CameraSource.Camera,
               quality : 60
           });

           this.previewUrl = photo.webPath;
        },
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