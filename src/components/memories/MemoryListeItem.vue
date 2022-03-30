<template>
    <ion-page>
        <ion-item  :router-link="`/memories/${memory.id}`" :key="memory.id">         
            <ion-thumbnail slot="start">
            <ion-img :src="memory.image" :alt="memory.title"></ion-img>
            </ion-thumbnail>
            <ion-label> {{memory.title}}</ion-label>
         </ion-item>
    </ion-page>
</template>

<script>
import {IonPage, IonItem, IonThumbnail, IonImg,IonLabel} from "@ionic/vue"
export default {
    props: ["memory"],
    components:{
        IonPage, IonItem, IonThumbnail, IonImg,IonLabel
    }
    
}
</script>