<template>
  <section id="projects" class="py-3 bg-light">
    <div class="container">
      <h1 class="text-center text-primary-emphasis fade-right">My Projects</h1>
      <p class="text-center mb-4 text-primary-emphasis fst-italic fade-right">Showcasing skills that deliver real-world results. Explore my portfolio to uncover the possibilities.</p>
      <div class="row">
        <div class="col-lg-3" v-for="project in projects" :key="project.id">
          <div class="card shadow-sm mb-2 bg-dark fade-left" style="border-radius: 26px;">
            <!-- Use paths that start with /img/ (relative to public directory) -->
            <img :src="`/img/projects/${project.image}`" class="card-img-top p-3" style="border-radius: 24px;" :alt="project.title" />
            <div class="card-body" style="border-top: 1px solid rgb(143, 201, 167);">
              <h6 class="card-title" style="color: rgb(109, 138, 139);">{{ project.title }}</h6>
              <p class="card-text" style="font-size: 12px; color: rgb(109, 138, 139);">{{ project.description }}
                <div class="d-flex justify-content-start gap-2 pt-2">
                  <img :src="`/img/stack/${project.img1}`" :alt="project.img1" width="8%" height="auto">
                  <img :src="`/img/stack/${project.img2}`" :alt="project.img2" width="8%" height="auto">
                  <img :src="`/img/stack/${project.img3}`" :alt="project.img3" width="8%" height="auto">
                  <img :src="`/img/stack/${project.img4}`" :alt="project.img4" width="8%" height="auto">
                  <img :src="`/img/stack/${project.img5}`" :alt="project.img5" width="8%" height="auto">
                  <img :src="`/img/stack/${project.img6}`" :alt="project.img6" width="8%" height="auto">
                  <img :src="`/img/stack/${project.img7}`" :alt="project.img7" width="8%" height="auto">
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
          image: "portfolio.png",  // Path relative to /public/img/projects
          link1: "#",
          link2: "#",
          img1: "bootstrap.svg",  // Path relative to /public/img/stack
          img2: "typescript.svg",
          img3: "vue.svg",
          img4: "vite.svg",
        },
        {
          id: 2,
          title: "Transaction Monitoring System",
          description: "The TMS streamlines visitor management, ticketing, and feedback with real-time tracking and color-coded tickets for efficiency and satisfaction.",
          image: "Tms.png",
          link1: "https://github.com/Jaymark-C-A/TransactionMonitoring",
          link2: "#",
          img1: "html.svg",
          img2: "css.svg",
          img3: "bootstrap.svg",
          img4: "javascript.svg",
          img5: "php.png",
          img6: "laravel.svg",
          img7: "mysql.svg",
        },
        {
          id: 3,
          title: "Car Rental Service Website",
          description: "A stylish and user-friendly car rental service, seamlessly powered by HTML and JavaScript, and designed with Bootstrap.",
          image: "CarRental.png",
          link1: "#",
          link2: "http://azrin.byethost12.com/Car%20Rental%20Service",
          img1: "html.svg",
          img2: "css.svg",
          img3: "bootstrap.svg",
          img4: "javascript.svg",
        },
        {
          id: 4,
          title: "Cleaning Service Website",
          description: "An efficient and polished cleaning service platform, expertly built with HTML and JavaScript, and styled using Bootstrap.",
          image: "Cleanex.png",
          link1: "#",
          link2: "http://azrin.byethost12.com/cleaning",
          img1: "html.svg",
          img2: "css.svg",
          img3: "bootstrap.svg",
          img4: "javascript.svg",
        },
      ],
    };
  },
};
</script>
