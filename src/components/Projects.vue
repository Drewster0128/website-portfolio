<script setup>

</script>

<template>
    <div class="page">
        <section class="hero">
            <h1 class="hero__title hero__title--red hero__title--left_align">Projects</h1>
            <p class="hero__paragraph hero__paragraph--left_align hero__paragraph--red">
                [Template] A collection of personal experiments, machine learning models, and data visualization tools exploring complex datasets and algorithmic solutions
            </p>
        </section>
        <section class="container container--column">
            <article class="project">
                <h2 class="project__title">Art Website</h2>
                <ul class="container container--column">
                    <li class="project__bullet">
                        Built an art portfolio website for my sister, Paige Cook, with Vite, React, and Typescript
                    </li>
                    <li class="project__bullet">
                        Deployed website onto Hostinger with a GitHub workflow triggered on push to main branch
                    </li>
                    <li class="project__bullet">
                        Scheduled a cron job using a Google Cloud service account and Google Cloud APIs to fetch artwork stored in the Drive and details stored in a Google Sheet
                    </li>
                    <li class="project__bullet">
                        Automatically resized images converted them to the webp file format in Python, dramatically reducing load times
                    </li>
                    <li class="project__bullet">
                        Upload new photos and metadata to site's public_html folder via FTP
                    </li>
                </ul>
                <ul class="container container--row">
                    <li class="project__technology">React</li>
                    <li class="project__technology">Vite</li>
                    <li class="project__technology">Typescript</li>
                    <li class="project__technology">Hostinger</li>
                    <li class="project__technology">Github</li>
                    <li class="project__technology">Python</li>
                    <li class="project__technology">CI/CD</li>
                </ul>
                <div class="container container--row">
                    <p class="project__status">Status: Ongoing</p>
                    <a class="project__repo" target="_blank" href="https://github.com/Drewster0128/paige-website">View Repo</a>
                </div>
            </article>
        </section>
    </div>
</template>