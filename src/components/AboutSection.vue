<template>
    <section id="about" class="py-5 bg-light">
      <div class="container">
        <div class="row">
          <div class="col-lg-7">
            <h1 class="text-center text-primary-emphasis mb-4 fade-right">About Me</h1>
            <p class="text-center text-primary-emphasis fs-6 fade-right">
              I'm Jaymark Azurin, Web Developer. My passion includes exploration, problem-solving, and fostering meaningful connections, while also prioritizing a balanced work-life approach. Guided by core values such as Integrity , Accountability, Kindness, and Leadership , I am dedicated to continuous improvement and making a positive impact on others.
            </p>
            <p class="text-center text-primary-emphasis fs-6 fade-right">
              I am actively involved in the creation of websites, encompassing a range of projects such as E-commerce websites, blogs, and advertising platforms. These endeavors serve as valuable opportunities for honing and advancing my programming skills. Additionally, I consistently explore innovative ideas to integrate into my projects, ensuring a dynamic and progressive approach to my programming practice.
            </p>
            
            <ul class="d-flex justify-content-center w-full px-0 gap-5 fade-right" style="font-size: 22px; font-weight: 700; list-style: none;">
              <li class="nav-item">
                  <a class="nav-link" style="color: #071e33;" href="https://www.facebook.com/jaymark.calma.14/"><i class="fab fa-facebook-f"></i></a>
              </li>
              <li class="nav-item">
                  <a class="nav-link" style="color: #071e33;" href="https://www.instagram.com/jay_azrin/"><i class="fab fa-instagram"></i></a>
              </li>
              <li class="nav-item">
                  <a class="nav-link" style="color: #071e33;" href="https://www.linkedin.com/in/jaymark-azurin-0a468729a/"><i class="fab fa-linkedin  "></i></a>
              </li>
              <li class="nav-item">
                  <a class="nav-link" style="color: #071e33;" href="https://github.com/Jaymark-C-A"><i class="fab fa-github"></i></a>
              </li>
            </ul>

             <div class="d-flex justify-content-center fade-right" >
              <button
                class="btn px-3 mr-5 py-2 shadow"
                style="border-radius: 5px; background: #071e33; color: rgb(143, 201, 167); font-weight: 600; font-size: 14px;"
                type="button"
                data-bs-toggle="modal"
                data-bs-target="#confirmationModal">
                Download my resume
              </button>

             </div>
          </div>
          <div class="col-lg-5 d-flex justify-content-center fade-left">
            <img class="d-none d-lg-block shadow" style="border: 1px solid rgb(143, 201, 167);" src="src/assets/img/Resume.png" alt="Resume" width="65%" height="90%">
          </div>
        </div>
        </div>
    </section>
  </template>
  
  <script lang="ts">
  import { onMounted, ref } from "vue";
  
  export default {
    name: "AboutSection",
    setup() {
      const elementsToAnimate = ref<HTMLElement[]>([]);
  
      onMounted(() => {
        elementsToAnimate.value = [
          ...document.querySelectorAll(".fade-right"),
          ...document.querySelectorAll(".fade-left"),
        ] as HTMLElement[];
  
        const observer = new IntersectionObserver(
          (entries) => {
            entries.forEach((entry) => {
              if (entry.isIntersecting) {
                entry.target.classList.add("visible");
                observer.unobserve(entry.target); // Stop observing once visible
              }
            });
          },
          { threshold: 0.1 } // Trigger when 10% of the element is visible
        );
  
        elementsToAnimate.value.forEach((element) => {
          observer.observe(element);
        });
      });
    },
  };
  </script>
  
  <style>
  /* You can also place CSS here if needed */
  </style>