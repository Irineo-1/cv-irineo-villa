<script setup lang="ts">
import Skills from "../interfaces/skills"

const props = defineProps<{ skills: any }>()

const skills: Skills[] = props.skills

</script>

<template>
    <section>
        <div>
            <h1>Habilidades</h1>
            <div class="every-skill">
                <p v-for="skill, i in skills" :key="i">{{ skill.name }}</p>
            </div>
        </div>
    </section>
</template>

<style>

.every-skill {
    margin-top: 10px;
    display: flex;
    flex-wrap: wrap;
}

.every-skill > p {
    background: #313131;
    padding: 4px 7px;
    color: white;
    margin-right: 10px;
    border-radius: 10px;
    line-height: 1rem;
}

</style>