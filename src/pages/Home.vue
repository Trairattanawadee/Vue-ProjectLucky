<template>
 <div>
    <navbar />
    <section class="home">


<div class="image">
    <img src="images/profile.png" alt="">
</div>

<div class="content">
    <h3>Hello, I'm Trairattanawadee Foythong</h3>
    <span>"Hope in the dark."</span>
    <p>Freelance For Graphics, Photography, Photoshop And Design And Create Avatars In VrChat,</p>
    <p>Is An Admin Of Cumcum's Avatar Page With Many Works To View,</p> 
    <p> Currently Studying In The Faculty Of Engineering Multimedia And Entertainment Bangkok University.</p> 
    
</div>

</section>
 </div>
</template>

<script>
import Navbar from '../components/Navbar.vue';
import axios from 'axios'


export default {
    components: { Navbar },
    methods: {
        async fetchExperience() {
            try {
                let res = await axios.get("https://633fc566e44b83bc73c0f545.mockapi.io/profile/v1/experiences")
                this.experience = res.data
            } catch (error) {
        
            }
        }
         
    },
    data() { 
        return { 
            experience: []
        }
    },
    beforeMount() {
        this.fetchExperience()
    }

            
    } 

</script>

<style>

</style>