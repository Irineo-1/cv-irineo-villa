<script setup lang="ts">
import Basics from "../interfaces/basics"

const props = defineProps<{ basics: any }>()

const Info: Basics = props.basics

</script>

<template>
    <section>
        <div>
            <h1>{{ Info.name }}</h1>
            <p>{{ Info.label }}</p>
            <a href="https://www.google.com/maps/place/Colima" class="container-location" target="_blank">
                <figure>
                    <img src="../assets/global.svg" alt="Location">
                </figure>
                <p>{{ Info.location.city }}, {{ Info.location.region }}</p>
            </a>
            <div class="container-contacs">
                <a :href="`mailto:${Info.email}`"><img src="../assets/email.svg" alt="Location"></a>
                <a :href="`${Info.github}`" target="_blank"><img src="../assets/github.svg" alt="github"></a>
                <a :href="`${Info.linkedin}`" target="_blank"><img src="../assets/linkedin.svg" alt="linkedin"></a>
            </div>
        </div>
    </section>
</template>

<style>
.container-location
{
    display: flex;
    align-items: center;
}

.container-location > figure > img {
    width: 1rem;
}

.container-contacs {
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-top: 10px;
}

a > img {
    width: 16px;
}

.container-contacs > a {
    display: flex;
    height: 32px;
    width: 32px;
    margin: 0px 5px;
    padding: 3px;
    border: 1px solid #e5e7eb;
    justify-content: center;
    align-items: center;
    border-radius: 5px;
}
</style>