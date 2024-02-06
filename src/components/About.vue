<script setup lang="ts">

const props = defineProps<{ aboutme: String }>()

const Info: String = props.aboutme

</script>

<template>
    <section>
        <div>
            <h1>Acerca de mi</h1>
            <p>{{ Info }}</p>
        </div>
    </section>
</template>

<style>

</style>