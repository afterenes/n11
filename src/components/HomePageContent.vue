<template>
    <div class="row">
        <div class="col-2"></div>

        <div class="col">
            <CarouselComponent />
            <MenuContenent />
            <ProductCard  />
            <CarouselDene />
            <MenuDene />
            <MallCompenent />
            
        </div>

        <div class="col-2"></div>
    </div>
</template> 

<script lang="ts">

import { defineComponent } from 'vue';
import CarouselComponent from './CarouselComponent.vue';
import MenuContenent from './MenuContenent.vue';
import ProductCard from './ProductCard.vue';
import CarouselDene from './CarouselDene.vue';
import MenuDene from './MenuDene.vue';
import MallCompenent from './MallCompenent.vue';



export default defineComponent({
    components: { CarouselComponent,MenuContenent, ProductCard,CarouselDene, MenuDene, MallCompenent  }
})
</script>