<script setup>

const props = defineProps(['title', 'bullets', 'technologies', 'status', 'repo'])

</script>

<template>
    <article class="project">
        <h2 class="project__title">{{ props.title }}</h2>
        <ul class="container container--column">
            <li class="project__bullet" v-for="bullet in props.bullets">
                {{ bullet }}
            </li>
        </ul>
        <ul class="container container--row container--wrap container--pad">
            <li class="project__technology" v-for="technology in props.technologies">
                {{ technology }}
            </li>
        </ul>
        <div class="container container--row container--between">
            <p class="project__status">Status: {{ props.status }}</p>
            <a class="project__repo" target="_blank" :href="props.repo">View Repo</a>
        </div>
    </article>
</template>