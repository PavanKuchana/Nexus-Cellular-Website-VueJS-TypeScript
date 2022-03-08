<template>
    <div class ="each-filter-container">
        <p class="filter-types-category">Colour
            <span class="material-icons expand-icon">keyboard_arrow_up</span>
        </p>
        <div class ="all-filter-items">
        <div class ="each-filter-item" v-for="each in ColourTypes" :key="each.id">
        <input :checked="each.isChecked" type="checkbox"  :name ="each.title" :id="each.title"  class ="checkbox">
        <label :for="each.title" class="filters-label">{{each.title}}</label>
        <p class ="available-count">{{each.availableCount}}</p>
        </div>
        </div>

    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
type ColourFilterType ={
    id:number  | string,
    title:string,
    availableCount:number | string,
    isChecked:boolean
}

export default defineComponent({
    name:'ColourFilter',
    setup(){

         const ColourTypes:ColourFilterType[]=[
            {
                id:1,
                title:"Blue",
                availableCount :29,
                isChecked:true,
                
            },
            {
                id:2,
                title:"Gray",
                availableCount :453,
                isChecked:false,
            },
            {
                id:3,
                title:"Brown",
                availableCount :17,
                isChecked:false,
            },
            {
                id:4,
                title:"Black",
                availableCount :99,
                isChecked:false,
            },
            {
                id:5,
                title:"White",
                availableCount :303,
                isChecked:false,
            },
            {
                id:6,
                title:"Green",
                availableCount :8,
                isChecked:false,
            },
        ]


       return {ColourTypes}
    }

})
</script>


<style scoped>

</style>