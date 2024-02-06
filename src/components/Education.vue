<script setup lang="ts">
import Education from "../interfaces/education"

const props = defineProps<{ education: any }>()

const educations: Education[] = props.education

</script>

<template>
    <section>
        <div>
            <h1>Educación</h1>
            <div class="every-education" v-for="education, i in educations" :key="i">
                <div class="container-enterprice-info">
                    <h4><a :href="`${education.url}`" target="_blank">{{ education.institution }} <img src="../assets/goto.svg"> </a></h4>
                    <p>{{ education.startDate }} - {{ education.endDate }}</p>
                </div>
                <span>{{ education.area }}</span>
            </div>
        </div>
    </section>
</template>

<style>

.every-education {
    margin-top: 10px;
}

.container-enterprice-info {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

a {
    color: black;
}

</style>