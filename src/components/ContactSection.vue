<template>
    <section id="contact" style="background-color: #071e33;">
      <div class="container py-5">
        <div class="row text-primary">
          <div class="col-lg-5 fade-right">
            <h2 class="mb-3">Send me a message!</h2>
            <form>
              <div class="mb-3">
                <label for="name" class="form-label">Name</label>
                <input type="text" id="name" class="form-control" placeholder="Enter your name" />
              </div>
              <div class="mb-3">
                <label for="email" class="form-label">Email</label>
                <input type="email" id="email" class="form-control" placeholder="Enter your email" />
              </div>
              <div class="mb-3">
                <label for="message" class="form-label">Message</label>
                <textarea id="message" class="form-control" rows="4" placeholder="Your message"></textarea>
              </div>
              <button type="submit" class="form-control btn btn-primary">Send</button>
            </form>
          </div>
          <div class="col-lg-7 text-light">
            <div class="py-1 px-4 my-3 fade-left" style="border: 1px solid gray; border-radius: 10px;">
              <p class="mb-0 text-primary" style="font-size: 48px; font-weight: 700;">Get in touch.</p>
              <p class="small">Considering to be in contact with me regarding a project? Perhaps collaboration? Or just about anything?</p>
            </div>
            <div class="py-1 px-4 fade-left" style="border: 1px solid gray; border-radius: 10px;">
              <p class="mb-0 text-primary" style="font-size: 38px; font-weight: 700;">Seeking Opportunities.</p>
              <p class="small">Through hands-on experience with various projects, I have refined my ability to deliver customized solutions that align with client needs. While I have not yet had formal job experience, I am confident in my skills and readiness to tackle challenging opportunities that align with my interests.</p>
              <p class="small">With the utmost sincerity, I am a dedicated programmer, eager to contribute my skills while seeking financial stability.</p>
              <p class="medium text-primary"><i class="fas fa-map-marker-alt fs-6 me-2"></i>Currently based in the Philippines.</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script lang="ts">
  export default {
    name: "ContactSection",
  };
  </script>
  