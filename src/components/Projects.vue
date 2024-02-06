<script setup lang="ts">
import Projects from "../interfaces/projects"

const props = defineProps<{ projects: any }>()

const projects: Projects[] = props.projects

</script>

<template>
    <section>
        <div>
            <h1>Proyectos</h1>
            <div class="every-proyect">
                <div v-for="project,i in projects" :key="i">
                    <h4><a :href="`${project.url}`" target="_blank">{{ project.name }}</a></h4>
                    <p>{{ project.description }}</p>
                    <div>
                        <p v-for="tecnologi,i in project.tecnologis" :key="i">{{ tecnologi }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style>

.every-proyect
{
    margin-top: 10px;
    display: flex;
    flex-wrap: wrap;
}

.every-proyect > div {
    padding: 10px;
    margin: 5px;
    width: calc(100% / 3.2);
    height: auto;
    border-radius: 10px;
    border: 1px solid #e5e7eb;
}

.every-proyect > div * {
    margin-top: 5px;
}

.every-proyect > div > div > p {
    margin-top: 0;
    background: #d1d1d1;
    color: black;
    padding: 3px 5px;
    line-height: 1rem;
    display: inline-block;
    border-radius: 5px;
    margin: 2px 2px;
}

a:hover {
    text-decoration-line: underline;
}

@media (max-width: 500px) {
    .every-proyect > div {
        width: 100%;

    }
}
</style>