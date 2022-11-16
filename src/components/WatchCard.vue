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

const emits = defineEmits(['epSelected'])

const handleContinueBtn = ()=>{
    console.log('episode selectionné: > ', props.epTitle)
    emits('epSelected',props.epTitle)
}


// va renvoyer une chaîne avec le format 
// EPO2SE12 
const epDisplay = computed(()=>{
    const ep = props.episode<10?'0'+props.episode:props.episode
    const season = props.season<10?'0'+props.season:props.season
    return `🐑${season}✨${ep}`
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
                <h6>{{epDisplay}}</h6>
                <h2>{{epTitle}}</h2>
                <button class="btn" @click="handleContinueBtn">Continue</button>
            </div>
        </div>  
    </div>
</template>

<style scoped>



</style>