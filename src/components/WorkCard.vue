<script setup>

const props = defineProps(['title', 'employer', 'bullets'])

</script>

<template>
    <article class="experience">
        <h2 class="experience__title">{{ props.title }}</h2>
        <h3 class="experience__employer">{{ props.employer }}</h3>
        <ul class="container container--column">
            <li class="experience__bullet" v-for="bullet in bullets">
                {{ bullet }}
            </li>
        </ul>
    </article>

</template>