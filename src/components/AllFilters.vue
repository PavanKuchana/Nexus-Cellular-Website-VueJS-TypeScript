<template>
    <div class ="filter-container">
        <div class="filters-heading">
        <p class="filter-text">Filter by:</p>
        <p class ="clear-text">Clear All</p>
        </div>
        <div class ="filtered-text-container">
            <p class ="filtered-text">Samsung<span class="material-icons">clear</span></p>
            <p class ="filtered-text">White<span class="material-icons">clear</span></p>
            <p class ="filtered-text">$250 - $900<span class="material-icons">clear</span></p>
            <p class ="filtered-text">On Sale<span class="material-icons">clear</span></p>
        </div>
         <p class="filter-types-category model">Model<span class="material-icons expand-icon">expand_more</span></p>
         <ProductTypeFilter/>
         <GradeTypeFilter/>
         <BrandFilter/>
         <ColourFilter/>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import ProductTypeFilter from '@/components/ProductTypeFilter.vue'
import GradeTypeFilter from '@/components/GradeTypeFilter.vue'
import BrandFilter from '@/components/BrandFilter.vue'
import ColourFilter from '@/components/ColourFilter.vue'
import '@/assets/global.css'

export default defineComponent({
    name:'AllFilters',
    components:{
        ProductTypeFilter,
        GradeTypeFilter,
        BrandFilter,
        ColourFilter
    }
})
</script>

<style scoped>
.filter-container{
    display: flex;
    flex-direction: column;
    width:290px;
}
.filters-heading{
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.filter-text{
    font-size:16px;
    font-weight: bold;
    color:#000000;
}
.clear-text{
    font-size:16px;
    font-weight: bold;
    color:#EE7A2D;
}
.filtered-text-container{
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    border-bottom: 1px solid #AAAAAA;
    padding-bottom:12px;
}

.filtered-text{
    display: flex;
    align-items: center;
    font-family:Arial, Helvetica, sans-serif;
    font-weight: bold;
    color:#000000;
    font-size:14px;
    background-color: #F3F3F3;
     border-radius:25px;
     padding:8px 10px 8px 10px;
     margin:5px;
}

span{
   color:#AAAAAA;
    margin-left:10px;
}
.model{
    border-bottom: 1px solid #AAAAAA;
}

@media screen and (max-width:992px){
    .filter-container{
        display: none;
    }
}

</style>