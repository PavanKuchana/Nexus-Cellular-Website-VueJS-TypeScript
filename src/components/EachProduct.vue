<template>
    <div class ="product-item-container">
        <img  class ="product-logo" :src="productItemDetails.productImage" :alt="productItemDetails.title"/>
        <div class ="product-item-info-container">
            <h2 class="product-name">{{productItemDetails.title}}</h2>
            <p class="product-model">{{productItemDetails.model}}</p>
            <div class="rating-info-container">
                <h3 class ="product-rating">{{productItemDetails.rating}}</h3>
                <img class ="rating-logo" :src="productItemDetails.ratingImage" :alt="productItemDetails.rating"/>
                <p class ="reviews-text">{{productItemDetails.reviewsCount}} Reviews</p>
            </div>
            <div class="info-container">
                <img class ="colors-logo" :src="productItemDetails.colorsImage" :alt="productItemDetails.color"/>
                <p class ="product-color-text">{{productItemDetails.color}} color</p>
            </div>
            <p class ="product-specifications">Operating system <span>{{productItemDetails.operatingSystem}}</span></p>
            <p class ="product-specifications">Display <span>{{productItemDetails.display}}</span></p>
            <p class ="product-specifications">Display resolution <span>{{productItemDetails.displayResolution}}</span></p>
            <p class ="product-specifications">CPU <span>{{productItemDetails.cpuDetails}}</span></p>
            <p class ="product-specifications">RAM size <span>{{productItemDetails.RAMInfo}}</span></p>
            <p class ="product-specifications">Built-in memory <span>{{productItemDetails.BuiltInMemory}}</span></p>
        </div>
        <div class ="product-price-quantity-details">
             <div class ="filter-icons">
                 <span class="material-icons icon">bar_chart</span>
                 <span class="material-icons icon">playlist_add</span>
             </div>
             <div class="price-details">
               <p :style="{color:'#7B7B7B',fontWeight: 'bold',marginBottom:'-20px'}">
                   {{productItemDetails.priceOne}}
                </p>
               <h2>{{productItemDetails.priceTwo}}</h2>
             </div>
             <div class ="info-container">
                 <div class ="quantity-container">
                 <button class ="button">-</button>
                 <p class="quantity-text">{{productItemDetails.quantity}}</p>
                 <button class ="button">+</button>
                 <span class="material-icons cart">shopping_cart</span>
                 </div>
             </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
import productItemType from '@/types/ProductItemType'

export default defineComponent({
    name:'EachProduct',
    props:{
        productItemDetails:{
            type:Object as PropType<productItemType>,
            required:true
        }
    },
})
</script>

<style scoped>
.product-item-container{
    border-bottom: 1px solid #AAAAAA;
    display: flex;
    justify-content: space-between;
}
.product-logo{
    width:320px;
    height:450px;
    margin:10px;
}
.product-item-info-container{
    width:400px;
    margin:10px 20px 20px 35px;
}
.product-price-quantity-details{
    margin:40px 25px 0px 30px;
    display: flex;
    flex-direction: column;
    align-items: flex-end;
}
.product-model{
    color:#7B7B7B;
    font-weight: bold;
    font-size:16px;
    margin-bottom: -5px;
}
.rating-info-container{
    display: flex;
    align-items: center;
    margin-bottom: -15px;
}
.info-container{
    display: flex;
    align-items: center;
    margin-bottom: -15px;
}
.rating-logo{
    height:25px;
    width:80px;
    margin-left:15px;
    margin-right:15px;
}
.reviews-text{
    font-size:16px;
    font-weight: bold;
    color:#EE7A2D;
}
 .product-name{
        font-size:18px;
    }
.product-color-text{
    margin-left: 20px;
}

.product-specifications{
    color:#C1C1C1;
    font-size:16px;
    font-weight: 500;
}

span{
    color:#000000;
    margin-left:5px;
}
.filter-icons{
    margin-bottom: 30px;
    display: flex;
    align-items: center;
}
.quantity-container{
    background-color: #F3F3F3;
    height: 35px;
    width:140px;
    padding:10px;
    border-radius: 25px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.quantity-text{
    margin-right: 5px;
    margin-left:5px;
    color:#7B7B7B;
    font-weight: bold
}
.button{
    color:#AAAAAA;
    font-size: 16px;
    border:none;
    outline:none;
    background-color: transparent;
}

.cart{
    background-color:#EE7A2D;
    color:#ffffff;
    padding:5px 15px 5px 15px;
    border-radius:20px;
}

.icon{
     color:#C1C1C1;
}

.price-details{
   text-align: end;
}
@media screen and (max-width:992px){
    .product-logo{
        height:160px;
        width:174px;
        align-self: center;
        margin:0px;
    }
    .product-item-container{
        border-right: 1px solid #AAAAAA;
        border-top: 1px solid #AAAAAA;
        width:100%;
        height:400px;
        padding-bottom: 5px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }
    .product-item-info-container{
        width:100%;
        margin:5px;
    }
    .product-name{
        font-size:14px;
        width:120px;
        margin-top:-30px;
    }
    .product-model{
        display: none;
    }
    .product-specifications{
        display: none;
    }
    .product-color-text{
        display: none;
    }
    .rating-info-container{
        display: none;
    }
    .filter-icons{
        display: none;
    }
    .colors-logo{
        height:20px;
        width:40px;
    }
   .product-price-quantity-details{
       align-items: flex-start;
       margin:40px 0px 0px 10px;
   }
    .price-details{
        text-align: start;
        margin-top:-50px;
    }
    .quantity-container{
        margin-bottom:10px;
        width:120px;
        padding:5px;
    }
    .cart{
       padding:2px 5px 2px 5px;
    }
}

</style>



