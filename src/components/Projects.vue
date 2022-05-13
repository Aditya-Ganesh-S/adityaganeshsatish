<template>
  <section class="projects">
    <h1 class="projects__heading">Projects</h1>
    <div class="projects__container">
      <Project
        v-for="project in projects"
        :key="project.id"
        :project="project"
      />
    </div>
  </section>
</template>

<script>
import Project from "./Project.vue";
import MusicImage from "../assets/img/Music.jpg";
import EzFlight from "../assets/img/EzFlight.jpg";
import CoronaVirus from "../assets/img/coronaVirus.jpg";
import MyStudyCircle from "../assets/img/studyCircle.jpg";
import ExpenseTracker from "../assets/img/expenseTracker.jpg";
import BabyHealthStimulator from "../assets/img/BabyHealth.jpg";
import Vue from "../assets/img/vue.svg";
import Firebase from "../assets/img/Firebase.svg";
import Hibernate from "../assets/img/hibernate.svg";
import JavaServlet from "../assets/img/JSP.svg";
import Jest from "../assets/img/jest.svg";
import Junit from "../assets/img/Junit.jpeg";
import React from "../assets/img/react.svg";
import Spring from "../assets/img/spring.svg";
import Sass from "../assets/img/sass.svg";
import Express from "../assets/img/express.svg";
import Html from "../assets/img/Html.png";
import Javascript from "../assets/img/JS.jpg";
import Css from "../assets/img/css.png";
import Java from "../assets/img/java.svg";
import NodeJs from "../assets/img/nodejs.svg";
import Mysql from "../assets/img/mysql.svg";
import MongoDb from "../assets/img/mongo.svg";
import Tailwind from "../assets/img/tailwind.svg";

export default {
  components: {
    Project,
  },
  data() {
    return {
      visibleIndex: 0,
      projects: [
        {
          id: 1,
          title: "My Music Channel",
          duration: "Feb 2022 - Apr 2022",
          discription: [
            "A Java-based Simulator to map the evolution of SARS-COV-2 using the Genetic Algorithm",
            "Simulated the effect of the virus on 4 different human Genotypes by considering factors like human fitness, virus fitness, and Vaccine.",
            "Increased the performance of the application with the usage of multi-threading",
            "Simulated statistical data and illustrated it using graphs",
          ],
          techStack: [Vue, Firebase, Jest, Tailwind],
          projectImage: MusicImage,
          url: "https://github.com/Aditya-Ganesh-S/MusicApp",
        },
        {
          id: 2,
          title: "EzFlight",
          duration: "Jul 2021 - Aug 2021",
          discription: [
            "Flight management application built using Spring MVC, hibernate, & MySQL",
            "Used AJAX calls to perform client-side validation and to reduce bandwidth usage",
            "Users get email confirmation after booking and can download booking confirmation as PDF",
          ],
          techStack: [Spring, Mysql, Hibernate, JavaServlet],
          projectImage: EzFlight,
          url: "https://github.com/Aditya-Ganesh-S/Musicpp",
        },
        {
          id: 3,
          title: "covid evolution simulator",
          duration: "Jul 2021 - Aug 2021",
          discription: [
            "A Java-based Simulator to map the evolution of SARS-COV-2 using the Genetic Algorithm",
            "Simulated the effect of the virus on 4 different human Genotypes by considering factors like human fitness, virus fitness, and Vaccine.",
            "Increased the performance of the application with the usage of multi-threading",
            "Simulated statistical data and illustrated it using graphs",
          ],
          techStack: [Java, Junit],
          projectImage: CoronaVirus,
          url: "https://github.com/Aditya-Ganesh-S/SARS-Cov-2-Virus-Evolution-Simulator",
        },
        {
          id: 4,
          title: "MyStudyCircle",
          duration: "Jul 2021 - Aug 2021",
          discription: [
            "Developed a full-stack course management web-application employing React Js, Node Js, Express Js and MongoDB",
            "Implemented HTTP REST API and leveraged Fetch API for CRUD operations",
            "Employed MVC Architecture with Authentication & Authorization middleware using JSON WebToken",
          ],
          techStack: [React, NodeJs, Express, MongoDb, Sass],
          projectImage: MyStudyCircle,
          url: "https://github.com/Aditya-Ganesh-S/MyStudyCircle",
        },
        {
          id: 5,
          title: "Expense Tracker",
          duration: "Jul 2021 - Aug 2021",
          discription: [
            "Responsive Front End expense tracker web application built using React.",
            "Used React Hooks for managing state",
            "Developed responsive Chart Component for expenses visualization purposes.",
          ],
          techStack: [React],
          projectImage: ExpenseTracker,
          url: "https://github.com/Aditya-Ganesh-S/Expense-Tracker-React",
        },
        {
          id: 6,
          title: "BabyHealthStimulator",
          duration: "Jul 2021 - Aug 2021",
          discription: [
            "Spearheaded a full stack web application that assists pregnant women to track, maintain and improve their health using interactive questionnaire",
            "Remodeled a flexible schema using MongoDB to store and track health-related data ofusers",
            "Embodied HTTP REST API for CRUD Operations and applied MVC Architecture with Authentication & Authorization middleware using Passport.js",
          ],
          techStack: [Html, Css, Javascript, NodeJs, Express, MongoDb],
          projectImage: BabyHealthStimulator,
          url: "https://github.com/AdityaGanesh98/BabyHealth-Stimulator",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "@/assets/_shared.scss";
@import "@/assets/_projects.scss";
</style>