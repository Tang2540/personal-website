<template>
  <NavBar/>

  <section class="intro">
    <div id="hi">Hi, I'm</div>
    <div id="pathanin">Pathanin Mapunya</div>
    <a href="https://github.com/Tang2540" class="github-icon"></a>
  </section>

  <section class="about" id="about">
    <div class="headline" v-motion-fade>About Me</div>
    <div class="education">
      <div id="edu">Education</div>
      <div id="tu">
      <div>Thammasat University</div>
      <div>BBA in Management Information System</div>
      </div>
      <div id="sarasas">
        <div>Sarasas Witead Saimai School</div>
        <div>High-School Diploma (Arts-Math)</div>
      </div>
    </div>
    <p> I'm a student at Thammasat Business School. I've always been fascinated by coding, which led me to pursue a coding-related career. I am committed to pushing boundaries, embracing new technologies, and making meaningful contributions to the ever-evolving tech landscape.</p>
  </section>

  <section class="expertise" id="expertise">
    <div class="headline">Specialties</div>
    <Expertise/>
  </section>

  <section class="projects" id="projects">
    <div class="headline">Projects</div>
    <Projects/>
  </section>

  <section class="certificates" id="certificates">
    <div class="headline">Certificates</div>
    <Certificates/>
  </section>

  <section class="contact" id="contact">
    <div class="headline">Contact</div>
    <Contact/>
  </section>

  <section>
    <p></p>
  </section>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Expertise from './components/Expertise.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'
import Certificates from './components/Certificates.vue'

export default {
  name: 'App',
  components: {
    NavBar,Expertise,Projects,Certificates,Contact
  }
}
</script>

<style>
#app {
  font-family: "Poppins", sans-serif; 
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin:0;
  padding:0;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

#hi {
  font-size: 4rem;
  animation: slide-up 1.2s;
  animation-fill-mode: backwards;
}

#pathanin {
  font-size: 5rem;
  font-weight: 600;
  animation: slide-up 1.2s 0.2s;
  animation-fill-mode: backwards;
}

@keyframes slide-up {
  from {transform: translateY(100%);opacity:0;}
  to {transform: translateY(0%);opacity:1}
}

.intro {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1.5rem;
}

a,.btn {
  transition: all 0.3s ease
}

a{
  text-decoration: none;
  color: black;
}


.github-icon {
  width: 2rem;
  height: 2rem;
  background-image: url('@/assets/github-mark.png');
  background-size: cover;
  animation: slide-up 1.2s 0.4s;
  animation-fill-mode: backwards;
}

.about, .expertise, .projects, .certificates,.contact {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.headline {
  margin-bottom: 5rem;
  font-weight: 600;
  font-size: 3rem;
}

.education {
  display: flex;
  align-items: center;
  flex-direction: column;
  border: solid 2px black;
  padding: 2rem;
  border-radius: 50px;
}

#edu {
  font-weight: 600;
  font-size: 1.25rem;
}

#tu,#sarasas {
  display: flex;
  align-items: center;
  flex-direction: column;
  margin-top: 1rem;
}

#tu div:first-child,#sarasas div:first-child {
  font-weight: 600;
}

p {
  width: 65%;
  margin-top: 2rem;
}

.expertise, .projects, .certificates,.contact {
  margin-top: 10rem;
}

@media only screen and (max-width: 1024px) {
  #pathanin {
    font-size: 4rem;
  }

}

@media only screen and (max-width: 768px) {
  #pathanin {
    font-size: 3rem;
  }
}

@media only screen and (max-width: 576px) {
  #hi {
    font-size: 1.5rem;
  }

  #pathanin {
    font-size: 2rem;
  }

  .education {
    padding: 10px;
  }
}
</style>
