<template>
    <div class="each-filter-container">
        <p class="filter-types-category">Product Type
            <span class="material-icons expand-icon">keyboard_arrow_up</span>
        </p>
         <div class ="all-filter-items">
        <div class ="each-filter-item" v-for="each in productTypes" :key="each.id">
        <input :checked="each.isChecked" type="checkbox" :name ="each.title" :id="each.title" class ="checkbox">
        <label :for="each.title" class="filters-label">{{each.title}}</label>
        <p class ="available-count">{{each.availableCount}}</p>
        </div>
        </div>

    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
type productTypes ={
    id:number  | string,
    title:string,
    availableCount:number | string,
    isChecked:boolean
}

export default defineComponent({
    name:'ProductTypeFilter',
    setup(){

        const productTypes:productTypes[]=[
            {
                id:1,
                title:"Adhesives",
                availableCount :42,
                isChecked:false,
            },
            {
                id:2,
                title:"Antennas",
                availableCount :241,
                isChecked:false,
            },
            {
                id:3,
                title:"Battery Covers",
                availableCount :17,
                isChecked:false,
            },
            {
                id:4,
                title:"Board ICs",
                availableCount :8,
                isChecked:false,
            },
            {
                id:5,
                title:"Brackets",
                availableCount :1303,
                isChecked:false,
            }
        ]


       return {productTypes}
    }

})
</script>


<style scoped>

</style>