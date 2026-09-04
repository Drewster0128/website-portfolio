<script setup>
import Home from "./components/Home.vue"
import WorkExperience from './components/WorkExperience.vue';
import Projects from './components/Projects.vue';
import NavBar from './components/NavBar.vue';

import { ref, useTemplateRef, onMounted, nextTick } from "vue";

const home = useTemplateRef('home');
const work = useTemplateRef('work');
const projects = useTemplateRef("projects");

const currentPage = ref("home");

onMounted(() => {

  let firstload = true;

  const observer = new IntersectionObserver(entries => {
    const screenHeight = window.screen.height;
    if(firstload) {
      firstload = false;
      return;
    }
    else {
      entries.forEach((entry) => {
        if(entry.intersectionRect.height > 0.80 * screenHeight) {
          if(entry.target.id != currentPage.value) {
            currentPage.value = entry.target.id;
          }
        }
      })
    }

  }, {
    threshold: Array.from({length: 101}, (_, i) => i / 100)
  })
  
  const lazyloadobserver = new IntersectionObserver((entries, observer) => {
    const screenHeight = window.screen.height;
    if(firstload) {
      firstload = false;
      return; 
    }
    else {
      entries.forEach((entry) => {
        console.log("hi");
        if(entry.intersectionRect.height > 0.80 * screenHeight) {
          console.log(entry.target.classList);
          if(entry.target.classList.contains("hidden")) {
            entry.target.classList.remove("hidden");
            observer.unobserve(entry.target);
          }
        }
      })
    }
  }, {
    threshold: Array.from({length: 101}, (_, i) => i / 100)
  })

  observer.observe(home.value.target);
  observer.observe(work.value.target);
  observer.observe(projects.value.target);

  lazyloadobserver.observe(home.value.target);
  lazyloadobserver.observe(work.value.target);
  lazyloadobserver.observe(projects.value.target);
})

</script>

<template>
  <NavBar :active_page="currentPage"/>
  <Home ref="home"/>
  <WorkExperience ref="work"/>
  <Projects ref="projects"/>
</template>
