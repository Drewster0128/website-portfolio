<script setup>

const props = defineProps(["active_page"]);
import Resume from "../assets/AndewSCookResume-Generic-8-21-26.pdf";


</script>

<template>
    <header class="header container container--row container--between container--align_baseline">
        <div class="column column--fle invisble md_display--visible">
            <h2 class="nav__title">Andrew Cook</h2>
        </div>
        <nav class="nav column column--flex-2 container container--row container--center md_flex_grow--1">
            <a class="nav__item" :class="{ 'nav__item--selected': props.active_page === 'home' }" href="#home">Home</a>
            <a class="nav__item" :class="{ 'nav__item--selected': props.active_page === 'work' }" href="#work">Work</a>
            <a class="nav__item" :class="{ 'nav__item--selected': props.active_page === 'projects' }" href="#projects">Projects</a>
        </nav>
        <div class="column column--flex column--end">
            <a class="nav__button" target="_blank" :href="Resume">Resume</a>
        </div>
    </header>
</template>