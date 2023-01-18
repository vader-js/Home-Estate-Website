<template>
  <div class="propertywrapper">
    <div class="topic">
        <hi class="top">List Of Properties</hi>
        <button>view all properties</button>
    </div>
    <div class="property" v-for="property in properties" :key="property.id">
        <div class="propertyimage">
            <img :src="property.img" alt="">
        </div>
        <div class="propertybody">
            <hi class="location">{{property.location}}</hi>
            <p class="title">{{property.title}}</p>
            <h2 class="price">{{property.price}}</h2>
            <div class="bottom">
                <span class="phone">{{property.phone}}</span>
                <span class="water">{{property.water}}</span>
                <span class="electricity">{{property.electricity}}</span>
            </div>
        </div>
    </div>
    <footer class="pagination"></footer>
  </div>
</template>

<script>
import { property } from "../assets/file.js"
import { ref } from '@vue/reactivity'
export default {
    name: 'Propertypage',
    setup() {
        const properties = ref(property)
        return {
            properties
        }
    }

}
</script>

<style>

</style>