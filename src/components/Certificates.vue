<script setup lang="ts">
import Certificates from "../interfaces/certificates"

const props = defineProps<{ certificados: any }>()

const certificados: Certificates[] = props.certificados

</script>

<template>
    <section>
        <div>
            <h1>Certificaciones</h1>
            <div class="every-education" v-for="certificado, i in certificados" :key="i">
                <div class="container-enterprice-info">
                    <h4><a :href="`${certificado.url}`" target="_blank">{{ certificado.name }} <img src="../assets/goto.svg"></a></h4>
                    <p>{{ certificado.date }}</p>
                </div>
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