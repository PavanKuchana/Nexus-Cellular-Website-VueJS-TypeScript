<template>
    <div class ="each-filter-container">
        <p class="filter-types-category">Brand
            <span class="material-icons expand-icon">keyboard_arrow_up</span>
        </p>
        <div class ="all-filter-items">
        <div class ="each-filter-item" v-for="each in BrandTypes" :key="each.id">
        <input :checked="each.isChecked" type="checkbox" :name ="each.title" :id="each.title"  class ="checkbox">
        <label :for="each.title" class="filters-label">{{each.title}}</label>
        <p class ="available-count">{{each.availableCount}}</p>
        </div>
        <p class ="view-all-text">View All</p>
        </div>

    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
type BrandFilterType ={
    id:number  | string,
    title:string,
    availableCount:number | string,
    isChecked:boolean
}

export default defineComponent({
    name:'BrandFilter',
    setup(){

        const BrandTypes:BrandFilterType[]=[
            {
                id:1,
                title:"Apple",
                availableCount :29,
                isChecked:false
                
            },
            {
                id:2,
                title:"Samsung",
                availableCount :453,
                isChecked:true
            },
            {
                id:3,
                title:"LG",
                availableCount :17,
                isChecked:false
            },
            {
                id:4,
                title:"Sony",
                availableCount :99,
                isChecked:false
            },
            {
                id:5,
                title:"Huawei",
                availableCount :303,
                isChecked:false
            },
        ]


       return {BrandTypes}
    }

})
</script>


<style scoped>
.view-all-text{
    font-size:16px;
    font-weight: bold;
    color:#EE7A2D;
}
</style>