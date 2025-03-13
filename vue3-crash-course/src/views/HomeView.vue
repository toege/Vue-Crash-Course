<script setup>
import Hero from '@/components/Hero.vue';
import HomeCards from '@/components/HomeCards.vue';
import JobListings from '@/components/JobListings.vue';
</script>

<template>
    <Hero title="Test-Title" subtitle="Test subtitle" />
    <HomeCards title="Test-Title" subtitle="Test subtitle" />
    <JobListings :limit="3" :showButton="true" />  
</template>