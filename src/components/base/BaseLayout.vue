<template>
 <ion-page>
        <ion-header>
            <ion-toolbar>
                <ion-buttons slot="start">
                    <ion-back-button :default-href="defaultBackLink"> </ion-back-button>
                </ion-buttons>
                <ion-title> {{pageTitle}}</ion-title>
                <ion-buttons slot="end">
                    <slot name="actions-end"></slot>
                </ion-buttons>
            </ion-toolbar>
        </ion-header>
        <ion-content>
          <slot></slot>        
        </ion-content>
    </ion-page>
   
</template>

<script>
import {
    IonPage,
    IonHeader,
    IonTitle,
    IonContent,
    IonToolbar,
    IonBackButton,
    IonButtons,
   
    } from '@ionic/vue';

export default {
  props: ['pageTitle','defaultBackLink'],
    components:{
        IonPage,
        IonHeader,
        IonButtons,
        IonTitle,
        IonContent,
        IonToolbar,
        IonBackButton,
      
    },
    data(){
       return {
          
       }
    }
    
}
</script>