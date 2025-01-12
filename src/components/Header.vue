<template>
    <nav class="navbar navbar-expand-lg pt-3" style="font-family: Arial, Helvetica, sans-serif; background-color: #071e33;">
        <div class="container mb-5">
            <!-- Logo -->
            <img src="/src/assets/img/logo.png" class="navbar-brand fade-right" alt="logo">
    
            <!-- Navbar Toggler for Small Screens -->
            <button
                class="navbar-toggler border-0"
                style="filter: invert(1);"
                type="button"
                data-bs-toggle="collapse"
                data-bs-target="#navbarNav"
                aria-controls="navbarNav"
                aria-expanded="false"
                aria-label="Toggle navigation"
                >
                <span class="navbar-toggler-icon"></span>
            </button>

    
            <!-- Navbar Links -->
            <div class="collapse navbar-collapse px-4 fade-left" id="navbarNav">
                <ul class="navbar-nav ms-auto" >
                    <li class="nav-item">
                        <a class="nav-link" href="#about" style="color: rgb(143, 201, 167);">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#projects" style="color: rgb(143, 201, 167);">Projects</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#contact" style="color: rgb(143, 201, 167);">Contact</a>
                    </li>
                </ul>
            </div>
    
            <!-- Button for booking schedule -->
            <button  
            class="btn px-3 mr-5 py-2 d-none d-md-block fade-left" 
            style="border-radius: 5px; border: 1px solid rgb(143, 201, 167); color: rgb(143, 201, 167); font-weight: 600; font-size: 14px;" 
            type="button" 
            data-bs-toggle="modal"
            data-bs-target="#confirmationModal">
                Resume
            </button>

            <!-- Confirmation modal -->
            <div
            class="modal fade"
            id="confirmationModal"
            tabindex="-1"
            aria-labelledby="confirmationModalLabel"
            aria-hidden="true"
            >
            <div class="modal-dialog">
            <div class="modal-content bg-primary-subtle">
                <div class="modal-header">
                <h5 class="modal-title fs-6 text-primary-emphasis fw-bold" style="letter-spacing: 1px;" id="confirmationModalLabel">Resume_Azurin-Jaymark.pdf</h5>
                <button
                    type="button"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                ></button>
                </div>
                <div class="modal-body bg-dark text-light-emphasis text-center fs-5">
                <div class="d-flex justify-content-center">
                    <img class="shadow-lg" style="border: 1px solid rgb(143, 201, 167);" src="/src/assets/img/Resume.png" alt="Resume" width="50%" height="auto">
                </div>
                </div>
                <div class="modal-footer">
                <button
                    type="button"
                    class="btn fw-bold"
                    style="font-size: 14px; color: #071e33;"
                    data-bs-dismiss="modal"
                >
                    Close
                </button>
                <button
                    type="button"
                    class="btn w-25 btn-primary"
                    style="font-size: 14px;"
                    @click="downloadResume"
                    data-bs-dismiss="modal"
                >
                    Download
                </button>
                </div>
            </div>
            </div>
        </div>

        </div>
    </nav>
  </template>
  
  <script lang="ts">
  export default {
    name: "Header",
    methods: {
        // Method to handle the resume download
        downloadResume() {
        // Replace this URL with the actual path to the resume file
        const resumeUrl = '/src/assets/pdf/Resume_Azurin-Jaymark.pdf';

        // Create an anchor tag to trigger the download
        const link = document.createElement('a');
        link.href = resumeUrl;
        link.download = 'Resume_Azurin-Jaymark.pdf'; // Optionally change the file name
        document.body.appendChild(link);
        link.click();
        document.body.removeChild(link);
        }
    }
  };
  </script>
  
