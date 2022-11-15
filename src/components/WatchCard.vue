<script setup>

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


</script>

<template>
    <div class="courses-container">
        <div class="course">
            <div class="course-preview">
                <h6>Season {{season}}</h6>
                <h2>{{series}}</h2>
            </div>
            <div class="course-info">
                <h6>ep: S02E08</h6>
                <h2>{{epTitle}}</h2>
                <button class="btn" >Continue</button>
            </div>
        </div>  
    </div>
</template>

<style>
</style>