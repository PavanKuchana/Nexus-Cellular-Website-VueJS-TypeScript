<template>
    <div class ="each-filter-container">
        <p class="filter-types-category">Grade
            <span class="material-icons expand-icon">keyboard_arrow_up</span>
        </p>
        <div class ="all-filter-items">
        <div class ="each-filter-item" v-for="each in GradeTypes" :key="each.id">
        <input :checked="each.isChecked" type="checkbox"  :name ="each.title" :id="each.title"  class ="checkbox">
        <img  class="stars-image" :src="each.ratingImage" :alt="each.title"/>
        <label :for="each.title" class="filters-label">{{each.title}}</label>
        <p class ="available-count">{{each.availableCount}}</p>
        </div>
        </div>

    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
type GradeTypes ={
    id:number  | string,
    title:string,
    availableCount:number | string
    ratingImage:string,
    isChecked:boolean
}

export default defineComponent({
    name:'GradeTypeFilter',
    setup(){

        const GradeTypes:GradeTypes[]=[
            {
                id:1,
                title:"4 & up",
                availableCount :42,
                ratingImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646657113/4_star_rating_uhgyzw.jpg',
                isChecked:false
            },
            {
                id:2,
                title:"3 & up",
                availableCount :241,
                ratingImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646657119/3_stars_rating_tvo9oq.jpg',
                isChecked:false
            },
            {
                id:3,
                title:"2 & up",
                availableCount :17,
                ratingImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646657126/2_stars_rating_f08nzr.jpg',
                isChecked:false
            },
            {
                id:4,
                title:"1 & up",
                availableCount :8,
                ratingImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646657126/2_stars_rating_f08nzr.jpg',
                isChecked:false
            },
        ]


       return {GradeTypes}
    }

})
</script>


<style scoped>
.stars-image{
    width:90px;
}
</style>