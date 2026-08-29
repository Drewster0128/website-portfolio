<script setup>
import ProjectCard from './ProjectCard.vue';

const projects = [
    {
        title: 'Art Website',
        bullets: [
            "Built an art portfolio website for my sister, Paige Cook, with Vite, React, and Typescript",
            "Deployed website onto Hostinger with a GitHub workflow triggered on push to main branch",
            "Scheduled a cron job using a Google Cloud service account and Google Cloud APIs to fetch artwork stored in the Drive and details stored in a Google Sheet",
            "Automatically resized images converted them to the webp file format in Python, dramatically reducing load times",
            "Upload new photos and metadata to site's public_html folder via FTP"
        ],
        technologies: ["React", "Vite", "Typescript", "Hostinger", "Github", "Python", "CI/CD"],
        status: "Ongoing",
        repo: "https://github.com/Drewster0128/paige-website"
    },
    {
        title: 'Malicious Network Packet Classifier',
        bullets: [
            "Trained random forest model of 100 decision trees to classify malicious network packets",
            "Reduced model complexity by eliminating 200 highly correlated predictors",
            "Achieved Accuracy score of 97% with 5-fold cross validation",
            "Achieved Area Under Receiving Operating Characteristics Curve of 0.96"
        ],
        technologies: ["Python", "Pandas", "Numpy", "Google Colab", "scikit-learn", "Random Forest", "Recursive Feature Eliminator"],
        status: "Complete"
    }
]
</script>

<template>
    <div class="page page--circuit_board">
        <section class="hero">
            <h1 class="hero__title hero__title--red-on-white hero__title--left_align">Projects</h1>
            <p class="hero__paragraph hero__paragraph--left_align">
                [Template] A collection of personal experiments, machine learning models, and data visualization tools exploring complex datasets and algorithmic solutions
            </p>
        </section>
        <section class="container container--column">
            <ProjectCard v-for="project in projects" v-bind="project"/>
        </section>
    </div>
</template>