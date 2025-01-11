<template>
    <section id="projects" class="py-3 bg-light">
      <div class="container">
        <h1 class="text-center text-primary-emphasis fade-right">My Projects</h1>
        <p class="text-center mb-4 text-primary-emphasis fst-italic fade-right">Showcasing skills that deliver real-world results. Explore my portfolio to uncover the possibilities.</p>
        <div class="row">
          <div class="col-lg-3" v-for="project in projects" :key="project.id">
            <div class="card shadow-sm mb-2 bg-dark fade-left" style="border-radius: 26px;">
              <img :src="project.image" class="card-img-top p-3" style="border-radius: 24px;" :alt="project.title" />
              <div class="card-body" style="border-top: 1px solid rgb(143, 201, 167);">
                <h6 class="card-title" style="color: rgb(109, 138, 139);">{{ project.title }}</h6>
                <p class="card-text" style="font-size: 12px; color: rgb(109, 138, 139);">{{ project.description }}
                <div class="d-flex justify-content-start gap-2 pt-2">
                  <img :src="project.img1" :alt="project.img1" width="8%" height="auto">
                  <img :src="project.img2" :alt="project.img2" width="8%" height="auto">
                  <img :src="project.img3" :alt="project.img3" width="8%" height="auto">
                  <img :src="project.img4" :alt="project.img4" width="8%" height="auto">
                  <img :src="project.img5" :alt="project.img5" width="8%" height="auto">
                  <img :src="project.img6" :alt="project.img6" width="8%" height="auto">
                  <img :src="project.img7" :alt="project.img7" width="8%" height="auto">
                </div>
                </p>
                <div class="d-flex justify-content-start gap-2">
                  <a :href="project.link1" class="btn py-1" style="background-color: #071e33; color: rgb(143, 201, 167);" target="_blank"><i class="fab fa-github"></i></a>
                  <a :href="project.link2" class="btn py-1" style="background-color: #071e33; color: rgb(143, 201, 167);" target="_blank"><i class="fa-solid fa-arrow-up-right-from-square"></i></a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script lang="ts">
  export default {
    name: "ProjectsSection",
    data() {
      return {
        projects: [
          {
            id: 1,
            title: "Portfolio Website",
            description: "Seamlessly built with Vue for dynamic functionality and styled with Bootstrap for a polished and professional look.",
            image: "/src/assets/img/projects/portfolio.png",
            link1: "#",
            link2: "#",
            img1: "/src/assets/img/stack/bootstrap.svg",
            img2: "/src/assets/img/stack/typescript.svg",
            img3: "/src/assets/img/stack/vue.svg",
            img4: "/src/assets/img/stack/vite.svg",
          },
          {
            id: 2,
            title: "Transaction Monitoring System",
            description: "A stylish and user-friendly car rental service, seamlessly powered by HTML and JavaScript, and designed with Bootstrap.",
            image: "/src/assets/img/projects/Tms.png",
            link1: "https://github.com/Jaymark-C-A/TransactionMonitoring",
            link2: "#",
            img1: "/src/assets/img/stack/html.svg",
            img2: "/src/assets/img/stack/css.svg",
            img3: "/src/assets/img/stack/bootstrap.svg",
            img4: "/src/assets/img/stack/javascript.svg",
            img5: "/src/assets/img/stack/php.png",
            img6: "/src/assets/img/stack/laravel.svg",
            img7: "/src/assets/img/stack/mysql.svg",
          },
          {
            id: 3,
            title: "Car Rental Service Website",
            description: "A stylish and user-friendly car rental service, seamlessly powered by HTML and JavaScript, and designed with Bootstrap.",
            image: "/src/assets/img/projects/CarRental.png",
            link1: "#",
            link2: "http://azrin.byethost12.com/Car%20Rental%20Service",
            img1: "/src/assets/img/stack/html.svg",
            img2: "/src/assets/img/stack/css.svg",
            img3: "/src/assets/img/stack/bootstrap.svg",
            img4: "/src/assets/img/stack/javascript.svg",
          },
          {
            id: 4,
            title: "Cleaning Service Website",
            description: "An efficient and polished cleaning service platform, expertly built with HTML and JavaScript, and styled using Bootstrap.",
            image: "/src/assets/img/projects/Cleanex.png",
            link1: "#",
            link2: "http://azrin.byethost12.com/cleaning",
            img1: "/src/assets/img/stack/html.svg",
            img2: "/src/assets/img/stack/css.svg",
            img3: "/src/assets/img/stack/bootstrap.svg",
            img4: "/src/assets/img/stack/javascript.svg",
          },
        ],
      };
    },
  };
  </script>
  