<template>
<nav class = "nav-container">
    <span class="material-icons menu-icon">menu</span>
    <img class ="website-logo" src="https://res.cloudinary.com/dfzzwbmcq/image/upload/v1646643005/nexus_webiste_logo_m0yb9k.jpg"
    alt = "nexus-cellular-logo"/>
    <div class ="input-container">
        <input class ="input" type="search" placeholder="Search...">
        <div class ="search-options-container">
         <select class="search-category-info" name="NavOptions" id="">
            <option value="All Category">All Category</option>
        </select>
        <p class='material-icons search'>search</p>
        </div>
    </div>

    <div class ="all-options-container">
    <div class ="options">
    <span class="material-icons">person_outline</span>
    <p class ="options-text">Hi Stranger</p>
    </div>

    <div class ="options">
    <span class="material-icons">local_mall</span>
    <p class ="options-text">Quick Order</p>
    </div>

    <div class ="options">
    <span class="material-icons">shopping_cart</span>
    <p class ="options-text">Cart</p>
    </div>
    </div>
</nav>
<div class ="mobile-input-container">
        <input class ="input" type="search" placeholder="Search...">
        <div class ="search-options-container">
         <select class="search-category-info" name="NavOptions" id="">
            <option value="All Category">All Category</option>
        </select>
        <p class='material-icons search'>search</p>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name:'SecondNavbar'
})
</script>

<style scoped>
.nav-container{
    display: flex;
    align-items: center;
   
}
.website-logo{
    height:35px;
}
.input-container{
    background-color: #F3F3F3;
    height: 35px;
    width:70%;
    padding-left:20px;
    margin-left:20px;
    border-radius: 25px;
    border:none;
    outline:none;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.input{
    color:#AAAAAA;
    font-size: 16px;
    width:75%;
    border:none;
    outline:none;
    background-color: transparent;
}
.search-options-container{
    display: flex;
    align-items: center;
}
.search-category-info{
    color:#AAAAAA;
    font-family: "Roboto";
    font-size:16px;
    font-weight: 400;
    margin-right:25px;
    display: flex;
    align-items: center;
    padding-left:10px;
    border-left:2px #AAAAAA solid;
    background-color:transparent;
    border:none;
    outline: none;
}
.search{
    background-color:#EE7A2D;
    color:#ffffff;
    padding:5px;
    border-radius:25px;
}
.all-options-container{
    display: flex;
    align-items: center;
}
.options{
    text-align: center;
    margin-left:20px;
    margin-top:10px;
}

.options-text{
    color:#A2A2A2;
    font-family: "Roboto";
    font-size:12px;
    font-weight: 400;
    margin-top:-2px;
}
.icon{
    color:#878787;
    font-weight: bold;
    margin-left:5px;
    margin-right:5px;
}
.mobile-input-container{
    display: none;
}
.menu-icon{
    display: none;
}
@media screen and (max-width: 992px){
    .nav-container{
        width:100%;
        justify-content: space-between;
    }
    .input-container{
        display: none;
    }
    .options{
        margin-left:5px;
}
    .options-text{
        display: none;
    }
   
    .menu-icon{
        display: block;
        margin-right:15px;
        margin-top:5px;
    }
    
    .mobile-input-container{
        display: block;
        background-color: #F3F3F3;
        height: 35px;
        width:100%;
        margin-top:15px;
        padding-left:20px;
        border-radius: 25px;
        border:none;
        outline:none;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    
    
    .all-options-container{
        margin-left:10px;
    }
}

@media screen and (min-width:992px) and (max-width:1200px){
   .nav-container{
       width:1150px;
   }
}

</style>