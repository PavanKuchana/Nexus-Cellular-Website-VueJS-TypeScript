<template>
    <div class ="all-products-header">
        <p class="shown-items-text">Shown 251 items</p>
        <div class ="all-products-filter-options">
            <span class="material-icons icon">menu</span>
            <span class="material-icons">apps</span>
             <select class ="select-category" name="selectCategory" id="">
            <option value="Part Type Position">Part Type Position</option>
            </select>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name:'AllProductsHeader'
})
</script>

<style scoped>

.all-products-header{
    display: flex;
    align-items: center;
    justify-content: space-between;
    width:980px;
}
.all-products-filter-options{
    display: flex;
    align-items: center;
}
.select-category{
    background-color:#F3F3F3;
    height:35px;
    width:75%;
    border-radius: 20px;
    padding-left:10px;
    margin-left:20px;
    border:none;
    outline:none;
}
.shown-items-text{
     color:#C1C1C1;
    font-size:16px;
    font-weight: bold;
}

.icon{
    color:#EE7A2D;
    margin-right:10px;
}

@media screen and (max-width:992px){
    .all-products-header{
        display: none;
    }
}

</style>
