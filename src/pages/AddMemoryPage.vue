<template>
    <ion-page>
        <base-layout page-title="Add Memory" default-back-link="/memories">
            <creatememory-form></creatememory-form>
        </base-layout>
        
    </ion-page>
</template>

<script>
import {IonPage} from "@ionic/vue"
import CreatememoryForm from '../components/memories/CreatememoryForm.vue'
export default {
    components:{
        IonPage,
        CreatememoryForm
    }
    
}
</script>