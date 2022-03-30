<template>
  <ion-img :src="memory.image" :alt="memory.title"></ion-img>
  <h2 class="ion-text-center">{{memory.title}}</h2>
  <p class="ion-text-center">{{memory.body}}</p>
</template>

<script>
import {IonImg} from "@ionic/vue";

export default {
    props: ["memory"],
    components:{
        IonImg
    }

}
</script>

<style>

</style>