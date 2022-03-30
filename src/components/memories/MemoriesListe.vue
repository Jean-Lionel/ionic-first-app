<template>
    <ion-list>
        <memory-liste-item v-for="memory in memories"  :memory="memory" :key="memory.id">
        </memory-liste-item>
    </ion-list>
    
</template>

<script>
import { IonList} from "@ionic/vue";
import MemoryListeItem from './MemoryListeItem.vue';

export default {
    props:["memories"],
    components:{
        IonList,
        MemoryListeItem
    }
    
}
</script>