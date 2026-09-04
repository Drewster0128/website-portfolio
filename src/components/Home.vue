<script setup>
import { useIntersectionObserver } from "@vueuse/core";
import heroImg from "../assets/hero.png"
import {  ref, useTemplateRef, onMounted } from 'vue';

const target = useTemplateRef("target");

defineExpose({target})

</script>

<template>
    <div class="page page--circuit_board" id="home" ref="target">
        <!-- hero -->
        <section class="container container--column hero">
            <div class="row">
                <h1 class="hero__title">Andrew Cook</h1>
                <h2 class="hero__subtitle">IIT 2026</h2>
            </div>
            <div class="row">
                <p class="hero__paragraph">
                    [Template] Computer Science graduate specializing in scalable data architectures, machine learning models, and complex algorithmic problem-solving. Architecting solutions from raw data to actionable intelligence.
                </p>
            </div>
            <div class="container container--row container--center">
                <a href="#work" class="hero__button container container--row container--align_center">
                    Work Experience
                    <i class="button__icon bi bi-arrow-right-short"></i>
                </a>
                <a href="#projects" class="hero__button hero__button--black container container--row container--align_center">
                    Projects
                    <i class="button__icon bi bi-terminal"></i>
                </a>
            </div>
        </section>
        <!-- profile picture -->
        <section>
            <img class="profile_pic" :src="heroImg">
        </section>
        <!-- skills -->
        <section class="skills">
            <div class="container container--row container--between container--align_center container--mb-1">
                <h3 class="skills__title">Skills</h3>
                <i class="skills__icon bi bi-cpu"></i>
            </div>
            <ul class="container container--row container--wrap">
                <li class="skills__item">Data Structures</li>
                <li class="skills__item">Web Design</li>
                <li class="skills__item">Databases</li>
                <li class="skills__item">APIs</li>
                <li class="skills__item">Networks</li>
                <li class="skills__item">Linux</li>
                <li class="skills__item">Python</li>
                <li class="skills__item">Java</li>
                <li class="skills__item">MySQL</li>
                <li class="skills__item">SQL</li>
                <li class="skills__item">HTML</li>
                <li class="skills__item">CSS</li>
                <li class="skills__item">Javascript</li>
                <li class="skills__item">Typescript</li>
                <li class="skills__item">R</li>
                <li class="skills__item">React</li>
            </ul>
        </section>
    </div>
</template>

