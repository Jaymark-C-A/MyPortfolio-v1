<template>
  <section id="Stack" class="py-3">
    <div class="container">
      <div class="row">
        <div class="col-lg-2"></div>
        <div class="col-lg-8">
          <h1 class="text-center text-primary mb-4 fade-right">Technical Skills</h1>
          <div class="row">
            <div class="col-lg-2 mb-2" v-for="stack in Stack" :key="stack.id">
              <div class="card text-center text-light pt-2 pb-1 px-4 bg-transparent fade-left" style="border: 1px solid white; border-radius: 10px;">
                <!-- Directly referencing images in the public directory -->
                <img :src="`/img/stack/${stack.image}`" :alt="stack.title" class="pb-1 d-none d-lg-block" width="100%" height="auto">
                <p class="p-0 mb-0" style="font-size: 11px; font-weight: 600;">{{ stack.title }}</p>
              </div>
            </div>
          </div>
        </div>
<<<<<<< HEAD
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
        { id: 1, image: "html.svg", title: "HTML" },
        { id: 2, image: "css.svg", title: "CSS" },
        { id: 3, image: "bootstrap.svg", title: "Bootstrap" },
        { id: 4, image: "javascript.svg", title: "JavaScript" },
        { id: 5, image: "typescript.svg", title: "TypeScript" },
        { id: 6, image: "react.svg", title: "React" },
        { id: 7, image: "vue.svg", title: "Vue" },
        { id: 8, image: "vite.svg", title: "Vite" },
        { id: 9, image: "node.svg", title: "Node JS" },
        { id: 10, image: "php.png", title: "PHP" },
        { id: 11, image: "laravel.svg", title: "Laravel" },
        { id: 12, image: "mysql.svg", title: "MySQL" },
      ],
    };
  },
};
</script>
=======
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
            image: "./src/assets/img/stack/html.svg",
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
  
>>>>>>> 4aa2dd2ef18de725a2a296837630e0e79576d57d
