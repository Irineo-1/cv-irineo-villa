<script setup lang="ts">
import Work from "../interfaces/work"

const props = defineProps<{ work: any }>()

const works: Work[] = props.work

</script>

<template>
    <section>
        <div>
            <h1>Experiencia de trabajo</h1>
            <div class="every-work" v-for="work, i in works" :key="i">
                <div class="container-enterprice-info">
                    <h4>{{ work.name }}</h4>
                    <p>{{ work.startDate }} - {{ work.endDate }}</p>
                </div>
                <span>{{ work.position }}</span>
                <p>{{ work.summary }}</p>
            </div>
        </div>
    </section>
</template>

<style>

.every-work {
    margin-top: 10px;
}

.every-work * {
    margin: 10px 0px;
}

.container-enterprice-info {
    display: flex;
    align-items: center;
    justify-content: space-between;
}



</style>