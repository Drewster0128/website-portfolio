<script setup>

const props = defineProps(["active_page"]);


</script>

<template>
    <header class="header container container--row container--between container--align_end">
        <div class="column column--flex">
            <h2 class="nav__title">Andrew Cook</h2>
        </div>
        <nav class="nav column column--flex container container--row container--center">
            <a class="nav__item" :class="{ 'nav__item--selected': props.active_page === 'home' }" href="">Home</a>
            <a class="nav__item" :class="{ 'nav__item--selected': props.active_page === 'work' }" href="">Work</a>
            <a class="nav__item" :class="{ 'nav__item--selected': props.active_page === 'projects' }" href="">Projects</a>
            <a class="nav__item" href="">Contact</a>
        </nav>
        <div class="column column--flex column--end">
            <a class="nav__item nav__item--resume" href="">Resume</a>
        </div>
    </header>
</template>