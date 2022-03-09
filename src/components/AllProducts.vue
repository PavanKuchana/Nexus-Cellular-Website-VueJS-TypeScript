<template>
    <div class ="displaying-filters-products">
    <AllProductsHeader/>
    <div class ="displaying-products">
        <div v-for="each in productItemDetails" :key="each.id">
            <EachProduct :productItemDetails="each"/>
        </div>
    </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import AllProductsHeader from '@/components/AllProductsHeader.vue'
import EachProduct from '@/components/EachProduct.vue'
import productItemType from '@/types/ProductItemType'

export default defineComponent({
    name:'AllProducts',
    components:{
        AllProductsHeader,
        EachProduct
    },
    setup(){
        const productItemDetails:productItemType[]=[
            {
                id:1,
                productImage:'https://images.unsplash.com/photo-1611407019488-0a354195b618?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80',
                title:'Samsung Galaxy S21+ 5G 128GB (Grade A) (Handset Only)',
                model:'SKU:GH82-22131D',
                rating:'4.5',
                ratingImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646657113/4_star_rating_uhgyzw.jpg',
                reviewsCount:3614,
                colorsImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646717577/nexus_rating_colors_zhczwt.jpg',
                color:'White',
                quantity:23,
                priceOne:'$488.99',
                priceTwo:'$2139.49',
                operatingSystem:'Andriod 10',
                display:'6.53",IPS',
                displayResolution:'2340*1080',
                cpuDetails:'Mediatek Helio G80,2000Mgh, 8 core',
                RAMInfo:'4 Gb',
                BuiltInMemory:'64 Gb'
            },
            {
                id:2,
                productImage:'https://images.unsplash.com/photo-1611407019532-da1f63f4403e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80',
                title:'Samsung Galaxy Note 10 plus 256GB (Grade B) (Handset Only)',
                model:'SKU:GH82-22131D',
                rating:'4.5',
                ratingImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646657113/4_star_rating_uhgyzw.jpg',
                reviewsCount:3614,
                colorsImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646717577/nexus_rating_colors_zhczwt.jpg',
                color:'White',
                quantity:1,
                priceOne:'$488.99',
                priceTwo:'$531.49',
                operatingSystem:'Andriod 10',
                display:'6.53",IPS',
                displayResolution:'2340*1080',
                cpuDetails:'Mediatek Helio G80,2000Mgh, 8 core',
                RAMInfo:'4 Gb',
                BuiltInMemory:'64 Gb'
            },
            {
                id:3,
                productImage:'https://images.unsplash.com/photo-1597762470488-3877b1f538c6?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1480&q=80',
                title:'Samsung Galaxy S21 5G 128GB (Grade A) (Handset Only)',
                model:'SKU:GH82-22131D',
                rating:'4.5',
                ratingImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646657113/4_star_rating_uhgyzw.jpg',
                reviewsCount:3614,
                colorsImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646717577/nexus_rating_colors_zhczwt.jpg',
                color:'White',
                quantity:23,
                priceOne:'$488.99',
                priceTwo:'$719.49',
                operatingSystem:'Andriod 10',
                display:'6.53",IPS',
                displayResolution:'2340*1080',
                cpuDetails:'Mediatek Helio G80,2000Mgh, 8 core',
                RAMInfo:'4 Gb',
                BuiltInMemory:'64 Gb'
            },
            {
                id:4,
                productImage:'https://images.unsplash.com/photo-1611407019488-0a354195b618?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80',
                title:'Samsung Galaxy S21+ 5G 128GB (Grade A) (Handset Only)',
                model:'SKU:GH82-22131D',
                rating:'4.5',
                ratingImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646657113/4_star_rating_uhgyzw.jpg',
                reviewsCount:3614,
                colorsImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646717577/nexus_rating_colors_zhczwt.jpg',
                color:'White',
                quantity:23,
                priceOne:'$488.99',
                priceTwo:'$2139.49',
                operatingSystem:'Andriod 10',
                display:'6.53",IPS',
                displayResolution:'2340*1080',
                cpuDetails:'Mediatek Helio G80,2000Mgh, 8 core',
                RAMInfo:'4 Gb',
                BuiltInMemory:'64 Gb'
            },
            {
                id:5,
                productImage:'https://images.unsplash.com/photo-1611407019532-da1f63f4403e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80',
                title:'Samsung Galaxy Note 10 plus 256GB (Grade B) (Handset Only)',
                model:'SKU:GH82-22131D',
                rating:'4.5',
                ratingImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646657113/4_star_rating_uhgyzw.jpg',
                reviewsCount:3614,
                colorsImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646717577/nexus_rating_colors_zhczwt.jpg',
                color:'White',
                quantity:1,
                priceOne:'$488.99',
                priceTwo:'$531.49',
                operatingSystem:'Andriod 10',
                display:'6.53",IPS',
                displayResolution:'2340*1080',
                cpuDetails:'Mediatek Helio G80,2000Mgh, 8 core',
                RAMInfo:'4 Gb',
                BuiltInMemory:'64 Gb'
            },
            {
                id:6,
                productImage:'https://images.unsplash.com/photo-1597762470488-3877b1f538c6?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1480&q=80',
                title:'Samsung Galaxy S21 5G 128GB (Grade A) (Handset Only)',
                model:'SKU:GH82-22131D',
                rating:'4.5',
                ratingImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646657113/4_star_rating_uhgyzw.jpg',
                reviewsCount:3614,
                colorsImage:'https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646717577/nexus_rating_colors_zhczwt.jpg',
                color:'White',
                quantity:23,
                priceOne:'$488.99',
                priceTwo:'$719.49',
                operatingSystem:'Andriod 10',
                display:'6.53",IPS',
                displayResolution:'2340*1080',
                cpuDetails:'Mediatek Helio G80,2000Mgh, 8 core',
                RAMInfo:'4 Gb',
                BuiltInMemory:'64 Gb'
            }
        ]
        
        return {productItemDetails}
    }
})
</script>


<style scoped>
.displaying-filters-products{
    margin-left:30px;
}
.displaying-products{
    border: 1px solid #AAAAAA;
    border-radius:8px;
}

@media screen and (max-width:992px) {
    .displaying-filters-products{
        margin-left:0px;
    } 
    .displaying-products{
        border:none;
        display: flex;
        flex-wrap: wrap;
        width:100%;
   }
}

</style>