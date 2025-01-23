<template>
    <section style="font-family: Arial, Helvetica, sans-serif; background-color: #071e33; width: 100%; height: 60vh;">
      <div class="container pt-md-5 ">
            <div class="row">
                <div class="col-lg-2"></div>
                <div class="col-lg-6 pb-4 fade-left" style="border-left: 3px solid rgb(143, 201, 167); letter-spacing: 1px;">
                    <div class="mt-5" style="color: rgb(143, 201, 167); font-weight: 600; font-size: 14px;">
                        Hello, I'm
                    </div>
                    <div id="animated-text-container">
                        <div id="animated-text" class="mb-2" style="line-height: 40px; font-size: 40px; margin-bottom: -2px; color: rgb(197, 197, 197); font-weight: 600;"></div>                    
                    </div>
                    <div class="mb-3" style="line-height: 45px; font-size: 44px; color: rgb(109, 138, 139); font-weight: 600;">
                        I create web solutions.
                    </div>
                    <p class="w-md-100 p-0" style="font-size: 12px; line-height: 20px; color: rgb(109, 138, 139);">
                        I specialize in developing websites, including e-commerce sites, blogs, and advertising platforms, which help enhance my programming skills. I also actively seek new ideas to keep my approach dynamic and innovative.
                    </p>

                    <ul class="d-flex justify-content-between w-25 px-0 gap-4" style="font-size: 22px; font-weight: 700; list-style: none;">
                        <li class="nav-item">
                            <a class="nav-link" style="color: rgb(143, 201, 167);" href="https://www.facebook.com/jaymark.calma.14/"><i class="fab fa-facebook-f"></i></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" style="color: rgb(143, 201, 167);" href="https://www.instagram.com/jay_azrin/"><i class="fab fa-instagram"></i></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" style="color: rgb(143, 201, 167);" href="https://www.linkedin.com/in/jaymark-azurin-0a468729a/"><i class="fab fa-linkedin  "></i></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" style="color: rgb(143, 201, 167);" href="https://github.com/Jaymark-C-A"><i class="fab fa-github"></i></a>
                        </li>
                    </ul>

                    <a href="#projects" class="btn px-3 mb-5 py-2" style="border-radius: 5px; border: 1px solid rgb(143, 201, 167); color: rgb(143, 201, 167); font-weight: 600; font-size: 14px;">
                      View My Work <i class="fa fa-arrow-right"></i>
                    </a> 
                </div>
                <div class="col-lg-4"></div>
            </div>
        </div>
    </section>
  </template>
  
  <script lang="ts">
  import { defineComponent, onMounted } from "vue";
  
  export default defineComponent({
    name: "HeroSection",
    setup() {
      // Function to type text
      function typeText(
        text: string,
        targetElement: HTMLElement,
        callback?: () => void
      ) {
        let currentIndex = 0;
        targetElement.textContent = ""; // Clear the text content
  
        function typeNextChar() {
          if (currentIndex < text.length) {
            targetElement.textContent += text[currentIndex];
            currentIndex++;
            setTimeout(typeNextChar, 100); // Adjust typing speed here
          } else if (callback) {
            callback(); // Call the next part when finished
          }
        }
  
        typeNextChar();
      }
  
      // Function to initialize animation
      function initializeAnimation() {
        const textElement = document.getElementById("animated-text");
        if (!textElement) return;
  
        const textPart1 = "Jaymark Azurin";
        const textPart2 = "Full Stack Developer.";
  
        // Start typing the first part
        typeText(textPart1, textElement, () => {
          // Add a delay before typing the second part
          setTimeout(() => {
            textElement.classList.add("typed-text");
            typeText(textPart2, textElement, () => {
              // After text typing is complete, add the blinking cursor
              const cursor = document.createElement("span");
              cursor.classList.add("cursor");
              textElement.appendChild(cursor);
            });
          }, 500); // Adjust delay between parts
        });
  
        // Reset and reanimate every minute
        setInterval(() => {
          textElement.classList.remove("typed-text");
          textElement.textContent = ""; // Clear the text
          const cursor = textElement.querySelector(".cursor");
          if (cursor) cursor.remove(); // Remove the previous cursor
          typeText(textPart1, textElement, () => {
            setTimeout(() => {
              textElement.classList.add("typed-text");
              typeText(textPart2, textElement, () => {
                const newCursor = document.createElement("span");
                newCursor.classList.add("cursor");
                textElement.appendChild(newCursor);
              });
            }, 500);
          });
        }, 60000); // 1 minute in milliseconds
      }
  
      // Use Vue lifecycle hooks
      onMounted(() => {
        initializeAnimation();
      });
    },
  });
  </script>
  
  <style>
  /* Optional styles */
  
  .typed-text {
    color: #f8f9fa; /* Adjust text color if needed */
  }
  
  .cursor {
    display: inline-block;
    width: 3px;
    height: 1em;
    background-color: white;
    margin-left: 10px;
    animation: blink 0.7s steps(1) infinite;
  }
  
  @keyframes blink {
    50% {
      opacity: 0;
    }
  }
  </style>
  
