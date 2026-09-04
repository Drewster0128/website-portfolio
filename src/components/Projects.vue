<script setup>
import { useTemplateRef } from 'vue';
import ProjectCard from './ProjectCard.vue';

const target = useTemplateRef('target');

defineExpose({target});

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
    },
    {
        title: 'Third Time Through Order Penalty Analysis',
        bullets: [
            "Tracked velocity and spin rate over pitch count for starting pitchers in the 2025 MLB playogs",
            "Calculated starting pitchers' average OPS allowed for the n-th batter faced using play-by-play data",
            "Differenced each starting pitchers OPS allowed against the n-th batter to remove seasonal trend",
            "Smoothed velocity, spin rate, and digerenced OPS against to reduce impact of outliers with moving average",
            "Fitted each statistic into its own linear model and tested for a significant trend using the t-test"
        ],
        technologies: ["Python", "BeautifulSoup", "MatPlotLib", "Pandas", "Numpy", "Sklearn"],
        status: "Complete"
    },
    {
        title: "Matas Buzelis Player Comparison",
        bullets: [
            "Scraped post all-star game rookie splits for 29 stats on all NBA lottery picks from 2010 to 2025 with beautiful soup",
            "Rescaled raw stats in python between 0 and 1 to keep all statistics in the same range",
            "Transformed data using Principal Component Analysis, keeping columns with a cumulative explained variance at 90%",
            "Fitted data into a 10 nearest neighbor model based on Euclidean distance using sklearn",
            "Plotted the Euclidean distances of the 10 players closest resembling Matas’s stats into a bar graph with matplotlib"
        ],
        technologies: ["Python", "Pandas", "PCA", "MatPlotLib", "Numpy", "Sklearn", "BeautifulSoup"],
        status: "Complete",
        repo: "https://github.com/Drewster0128/nba-cluster"
    },
    {
        title: "Banking Program",
        bullets: [
            "Built an Entity-Relationship model linking important components of a banking service together, including customer information, employee data, physical locations, accounts, and all transactions between two accounts with a transaction number",
            "Translated an ER-model into functioning Postgres SQL tables and roles for all aspects in a bank account",
            "Coded backend in Java for bank account program to connect GUI with the SQL schema; including monthly statements, records of all transactions, and deposits or withdrawals from saving or checking accounts"
        ],
        technologies: ["Postgres SQL", "Java"],
        status: "Complete"
    }
]
</script>

<template>
    <div class="page page--circuit_board hidden" id="projects" ref="target">
        <section class="hero container container--column">
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