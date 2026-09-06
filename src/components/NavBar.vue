<script setup>

const props = defineProps(["active_page"]);
import Resume from "../assets/AndewSCookResume-Generic-8-21-26.pdf";

const resumeButtonHandler = () => {
    const dropDown = document.getElementById("resume_drop_down");
    dropDown.classList.toggle("drop_down--open");
}
</script>

<template>
    <header class="header container container--row container--between container--align_baseline">
        <div class="column column--flex">
            <h2 class="nav__title">Andrew Cook</h2>
        </div>
        <nav class="nav column column--flex container container--row container--center">
            <a class="nav__item" :class="{ 'nav__item--selected': props.active_page === 'home' }" href="#home">Home</a>
            <a class="nav__item" :class="{ 'nav__item--selected': props.active_page === 'work' }" href="#work">Work</a>
            <a class="nav__item" :class="{ 'nav__item--selected': props.active_page === 'projects' }" href="#projects">Projects</a>
            <a class="nav__item" href="">Contact</a>
        </nav>
        <div class="column column--flex column--end drop_down" id="resume_drop_down">
            <button class="drop_down__button" @click="resumeButtonHandler">
                Resume
                <i class="bi bi-chevron-right" id="arrow"></i>
            </button>
            <ul class="drop_down__menu">
                <li>
                    <a class="drop_down__item" :href="Resume">Generic</a>
                </li>
                <li>
                    <a class="drop_down__item" href="">Data Science</a>
                </li>
            </ul>
        </div>
    </header>
</template>