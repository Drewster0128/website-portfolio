<script setup>
import heroImg from "../assets/hero.png"
</script>

<template>
    <!-- hero -->
     <section class="hero">
        <div class="hero__title">
            <h1>Andrew Cook</h1>
            <h2>IIT 2026</h2>
        </div>
        <p class="hero__paragraph">
            [Template] Computer Science graduate specializing in scalable data architectures, machine learning models, and complex algorithmic problem-solving. Architecting solutions from raw data to actionable intelligence.
        </p>
        <div>
            <button class="hero__button">Work Experience</button>
            <button class="hero__button">Projects</button>
        </div>
     </section>
    <!-- profile picture -->
    <section class="profile_pic">
        <img :src="heroImg">
    </section>
    <!-- skills -->
    <section class="skills">
        <h3>Skills</h3>
        <ul>
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
</template>

