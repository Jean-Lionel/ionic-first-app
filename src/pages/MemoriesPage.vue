<template>
        <ion-page>
            <base-layout page-title="Bonjour tout le Monde">
                <ion-list>
                    <ion-item router-link="/memories/1">Lionel </ion-item>
                    <ion-item router-link="/memories/2">Lionel 2</ion-item>
                    <ion-item router-link="/memories/36">Lionel 36</ion-item>
                </ion-list>
            </base-layout>
        </ion-page>
       
</template>

<script>
import {IonPage,IonList, IonItem} from "@ionic/vue";

export default {
    components:{
        IonPage,
        IonList,
        IonItem
    },
    data(){
        return {
            memories : [
                {
                    id : "m1",
                    image : "",
                    title : "",
                    description : "",
                },
            ],

        }
    }  
}
</script>