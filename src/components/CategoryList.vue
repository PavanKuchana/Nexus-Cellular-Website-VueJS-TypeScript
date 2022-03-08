<template>
    <div class ="categories-bg-container">
         <div class ="categories">
        <p class ="category-text">Parts</p>
        <p class ="category-text">Accessories</p>
        <p class ="category-text active">Devices</p>
        <p class ="category-text">Buyback</p>
        <p class ="category-text offer">% Sales & Deals</p>
         <p class="material-icons icon">more_horiz</p>
         </div>
         <div class ="contact-container">
         <span class="material-icons">call</span>
         <p class ="contact">Hotline: <span>+1-877-614-1001</span></p>
         </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name:'CategoryList'
})
</script>

<style scoped>
.categories-bg-container{
    border-top:1px solid #FAFAFA;
    border-bottom: 2px solid #FAFAFA;
    height:40px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.categories{
    display: flex;
    align-items: center;
    justify-content: space-between;
    width:60%;
}
.category-text{
    font-size:18px;
    font-weight: bold;
    color:#000000;
}
.active{
    border-bottom:2px solid #EE7A2D;

}
.icon{
    color: #C4C4C4;
}
.offer{
  color:#BF4E46;
}
.contact{
     color:#A2A2A2;
    font-family: "Roboto";
    font-size:16px;
    font-weight: 400;
    margin-left:10px;
}
span{
    color:#7B7B7B;
    font-weight: bold;
}

.contact-container{
    display: flex;
    align-items: center;
}

@media screen and (max-width:992px){
    .categories-bg-container{
        display: none;
    }
}

@media screen and (min-width:992px) and (max-width:1200px){
   .categories-bg-container{
       width:1150px;
   }
}
</style>