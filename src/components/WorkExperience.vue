<script setup>
import { useTemplateRef } from 'vue';
import WorkCard from './WorkCard.vue';

const target = useTemplateRef('target');

defineExpose({target});

const experiences = [
    {
        title: "Data Science Intern",
        employer: "LabelMaster",
        bullets: [
            "Collaborated with a team of five to build an LSTM model using TensorFlow to forecast sales across multiple departments",
            "Connected seven trained LSTM models with frontend interface running with streamlit",
            "Scripted installation applications to ensure clean installs on all computers and laptops regardless of operating system",
            "Documented how-to guides describing step-by-step processes to output predictions and retrain models",
            "Visualized results using various graphs generated with Matplotlib",
            "Achieved average accuracy between all departments of 85-90%"   
        ]
    },
    {
        title: "IT Help Desk Intern",
        employer: "Clausen Miller P.C",
        bullets: [
            "Set up workstations for new employees with monitors, docking station, desk phones, ethernet, and access to office printers",
            "Assisted attorneys and secretaries over the phone for any tech related issues, including connecting to the company's VPN, installing drivers for personal printers, and teaching tips and tricks for Microsoft Office products like Word and Excel",
            "Wrote detailed descriptions on tickets defining the situation, who needed help, and how it was resolved",
            "Built a web user interface of printers and copiers separated by office location linking each printer to its status page for the IT staff to use on the company's intranet site",
            "Performed an audit on devices in the company's Active Directory, deleting any device that the company no longer uses, preventing any potential data breaches",
            "Consulted IT guides for common queries and updated them as needed"
        ]
    }
]
</script>

<template>
    <div class="page page--black hidden" id="work" ref="target">
        <section class="container container--column hero">
            <h1 class="hero__title hero__title--red-on-black">Work Experience</h1>
            <!--
            <p class="hero__paragraph hero__paragraph--red-on-black">[Template] A chronological ledger of professional developments, data architectures, blah blah blah</p>
            -->
        </section>
        <section class="container container--column">
            <WorkCard v-for="experience in experiences" v-bind="experience" />
        </section>
    </div>
</template>