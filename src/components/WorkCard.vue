<script setup>

const props = defineProps(['title', 'employer', 'bullets'])

</script>

<template>
    <article class="experience">
        <div class="container container--row container--between">
            <h2 class="experience__title">{{ props.title }}</h2>
            <i class="experience__icon bi bi-plus"></i>
        </div>
        <h3 class="experience__employer">{{ props.employer }}</h3>
        <ul class="container container--column">
            <li class="experience__bullet" v-for="bullet in bullets">
                {{ bullet }}
            </li>
        </ul>
    </article>

</template>