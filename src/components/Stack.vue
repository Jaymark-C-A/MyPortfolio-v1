<template>
    <section id="Stack" class="py-3">
      <div class="container">
        <div class="row">
          <div class="col-lg-2"></div>
          <div class="col-lg-8">
            <h1 class="text-center text-primary mb-4 fade-right">Technical Skills</h1>
            <div class="row">
              <div class="col-lg-2 mb-2" v-for="stacks in Stack" :key="stacks.id">
                <div class="card text-center text-light pt-2 pb-1 px-4 bg-transparent fade-left "  style="border: 1px solid white; border-radius: 10px;">
                  <img :src="stacks.image" :alt="stacks.title" class="pb-1 d-none d-lg-block" width="100%" height="auto">
                  <p class="pm-0 mb-0" style="font-size: 11px; font-weight: 600;">{{ stacks.title }}</p>
                </div>
              </div>
            </div>
          </div>
          <div class="col-lg-2"></div>
        </div>
        </div>
    </section>
  </template>
  
  <script lang="ts">
  export default {
    name: "Stack",
    data() {
      return {
        Stack: [
          {
            id: 1,
            image: require('@/assets/img/stack/html.svg'),
            title: "HTML",
          },
          {
            id: 2,
            image: "src/assets/img/stack/css.svg",
            title: "CSS",
          },  
          {
            id: 3,
            image: "src/assets/img/stack/bootstrap.svg",
            title: "Bootstrap",
          },
          {
            id: 4,
            image: "src/assets/img/stack/javascript.svg",
            title: "JavaScript",
          },
          {
            id: 5,
            image: "src/assets/img/stack/typescript.svg",
            title: "TypeScript",
          },
          {
            id: 6,
            image: "src/assets/img/stack/react.svg",
            title: "React",
          },  
          {
            id: 7,
            image: "src/assets/img/stack/vue.svg",
            title: "Vue",
          },
          {
            id: 8,
            image: "src/assets/img/stack/vite.svg",
            title: "Vite",
          },
          {
            id: 9,
            image: "src/assets/img/stack/node.svg",
            title: "Node JS",
          },
          {
            id: 10,
            image: "src/assets/img/stack/php.png",
            title: "PHP",
          },
          {
            id: 11,
            image: "src/assets/img/stack/laravel.svg",
            title: "Laravel",
          },
          {
            id: 12,
            image: "src/assets/img/stack/mysql.svg",
            title: "MySQL",
          },
        ],
      };
    },
  };
  </script>
  
