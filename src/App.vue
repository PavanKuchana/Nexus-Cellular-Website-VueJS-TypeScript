<template>
   <FirstNavbar/>
   <div class ="bg-container">
   <SecondNavbar/>
   <CategoryList/>
   <p class ="active-category-text">Nexus · Devices</p>
   <h1 class ="selected-category-text">Devices</h1>
   <p class="results">1-60 of 3,986 Results</p>

   <div class ="mobile-view-filter-container">
   <div class ="mobile-view">
     <input class ="checkBox" type="checkbox" name="checkbox" id="">
     <span class="material-icons icon">apps</span>
   </div>
   <div  class ="mobile-view">
   <p class ="filters-icon"><span class="material-icons">sort</span> Sort</p>
    <p class ="filters-icon"><span class="material-icons">playlist_add</span> Filters</p>
   </div>
   </div>
   
   <div class ="filters-products-section">
   <AllFilters/>
   <AllProducts/>
   </div>
   </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import FirstNavbar from './components/FirstNavbar.vue';
import SecondNavbar from './components/SecondNavbar.vue';
import CategoryList from './components/CategoryList.vue';
import AllFilters from './components/AllFilters.vue';
import AllProducts from './components/AllProducts.vue';

export default defineComponent({
  name: 'App',
  components: {
    FirstNavbar,
    SecondNavbar,
    CategoryList,
    AllFilters,
    AllProducts
  }
});
</script>

<style>
* {
  box-sizing: border-box;
}
body {
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen',
    'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue',
    sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.bg-container{
   padding-left:40px;
   padding-right:40px;
}

.active-category-text{
   color:#7B7B7B;
   font-weight: bold;
}
.filters-products-section{
  display: flex;
}

.results{
  display: none;
}
.mobile-view-filter-container{
  display: none;
}
.checkBox{
   display: none;
}

@media screen and (max-width:992px){
    .bg-container{
        padding-left:5px;
        padding-right:5px;
    }
    
    .selected-category-text{
        margin-bottom: -15px;
        margin-top:-10px;
    }
    .results{
      display: block;
       color:#C1C1C1;
      font-size:14px;
      font-weight: bold;
    }
    .mobile-view-filter-container{
      display: flex;
      align-items: center;
      width:100%;
      justify-content: space-between;
    }
    .mobile-view{
      display: flex;
      align-items: center;
    }
    .checkBox{
      display: block;
      height:20px;
      width:20px;
      border:1px solid #7B7B7B;
      border-radius:4px;
      margin-right:10px;
    }
    .filters-icon{
       display: flex;
      align-items: center;
      margin-left:15px;
      color:#000000;
      font-weight:bold
    }
    .icon{
    color:#EE7A2D;
    margin-right:10px;
   }

}

</style>
