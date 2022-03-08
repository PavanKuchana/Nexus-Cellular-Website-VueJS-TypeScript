<template>
    <nav class = "nav-container">
        <div class = "offers-container">
        
        <div class ="offer">
        <p class="material-icons icon">local_shipping</p>
        <p class = "nav-info">Free Shipping on orders over
            <span>$400</span>
        </p>
        </div>
         <div class ="offer">
         <p class='material-icons icon'>verified_user</p>
         <p class = "nav-info">Lifetime Warranty on Parts</p>
         </div>
         <div class ="offer">
        <p class="material-icons cutoff-icon">content_cut</p>
        <p class = "nav-info">Up to <span> 8pm </span> order Cutoffs</p>
        </div>
        </div>

        <div class = "offers-container">
        <select class="nav-info menu" name="NavOptions" id="">
            <option value="Knowledge Base">Knowledge Base</option>
        </select>
        <p class="nav-info menu">About Us</p>
        <p class="nav-info menu">Blog</p>
        <p class="nav-info">Contact Us</p>
        </div>

    </nav>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name:'FirstNavbar'
})
</script>

<style scoped>
 .nav-container{
        display: flex;
        align-items: center;
        justify-content: space-between;
        background-color:#F3F3F3;
        height:40px;
        padding-left:40px;
        padding-right:40px;
    }

@media screen and (max-width:992px) {
    .nav-container{
      display: none;
}
}
.offers-container{
    display: flex;
    align-items: center;
}

.offer{
    display: flex;
    align-items: center;
    margin-right:20px;
   
}
.icon{
    color:#EE7A2F;
    margin-right:10px;
}
.nav-info{
    color:#C1C1C1;
    background-color:transparent;
    font-size:14px;
    font-weight: 400;
    display: flex;
    align-items: center;
    border:none;
    outline: none;
}

.menu{
    margin-right:25px;
}
span{
    color:#878787;
    font-weight: bold;
    margin-left:5px;
    margin-right:5px;
}

.cutoff-icon{
     color:#EE7A2F;
     transform: rotate(270deg);
      margin-right:10px; 
}

@media screen and (min-width:992px) and (max-width:1200px){
   .nav-container{
       width:1235px;
   }
}


</style>