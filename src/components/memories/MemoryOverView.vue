<template>
  <ion-img :src="memory.image" :alt="memory.title"></ion-img>
  <h2>{{memory.title}}</h2>
  <p>{{memory.body}}</p>
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