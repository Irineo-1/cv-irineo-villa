<script setup lang="ts">

import cv from "./info/cv.json"
import Basics from "./components/Basics.vue";
import About from "./components/About.vue";
import Work from "./components/Work.vue";
import Education from "./components/Education.vue";
import Certificates from "./components/Certificates.vue"
import Skills from "./components/Skills.vue";
import Projects from "./components/Projects.vue";

</script>

<template>

<div class="container">
    <Basics :basics="cv.basics" />
    <About :aboutme="cv.basics.summary"/>
    <Work :work="cv.work" />
    <Education :education="cv.education" />
    <Certificates :certificados="cv.certificates" />
    <Skills :skills="cv.skills"/>
    <Projects :projects="cv.projects" />
</div>

</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
}
</style>
