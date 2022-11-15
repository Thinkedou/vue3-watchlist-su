<script setup>
import {computed} from "vue"

const props = defineProps({
    epTitle:{
        type:String
    },
    series:{
        type:String
    },
    episode:{
        type:Number
    },
    season:{
        type:Number
    }
})

const epDisplay = computed(()=>{
    return 'computed!'
})



</script>

<template>
    <div class="courses-container">
        <div class="course">
            <div class="course-preview">
                <h6>Season {{season}}</h6>
                <h2>{{series}}</h2>
            </div>
            <div class="course-info">
                <h6>ep: {{epDisplay}}</h6>
                <h2>{{epTitle}}</h2>
                <button class="btn" >Continue</button>
            </div>
        </div>  
    </div>
</template>

<style>
</style>