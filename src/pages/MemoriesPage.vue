<template>
    <ion-page>
        <ion-header>
            <ion-toolbar>
                <ion-title>
                Je suis en bonne santé
                 </ion-title>
            </ion-toolbar>
            
        </ion-header>
        <ion-content>
            <ion-list>
                <ion-item>Lionel</ion-item>
                <ion-item>Lionel 2</ion-item>
                <ion-item>Lionel 3</ion-item>
            </ion-list>
        </ion-content>

    </ion-page>
</template>

<script>
import {IonPage,IonHeader,IonTitle, IonContent, IonList, IonItem, IonToolbar} from '@ionic/vue';

export default {
    components:{
        IonPage,
        IonHeader,
        IonTitle,
        IonContent,
        IonList,
        IonItem,
        IonToolbar
    }
    
}
</script>