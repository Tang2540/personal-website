<template>
    <div class="grid-container">
        <div v-for="(project,index) in projects" :key="index" class="project">
          <div :class="`img${index}`" class="project-image"></div>
          <div class="project-name">{{project.name}}</div>
          <p>{{ project.desc }}</p>
          <a :href="links[index]">See the project on GitHub</a>
        </div>
    </div>
</template>

<style scoped>
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 20px;
    padding-left: 6rem;
    padding-right: 6rem;
}

.project {
  border: solid 2px black;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 10px;
}

.project-image {
  width: 15rem;
  height: 13rem;
  background-size:contain;
  background-repeat: no-repeat;
}

.img0 {
  background-image: url('@/assets/personal_web.png');
}

.img1 {
  background-image: url('@/assets/photon.png');
}

.project-name {
  font-weight: 600;
  font-size: 1.23rem;
}

a {
  border-radius: 500px;
  border: solid 2px black;
  padding: 5px;
  color: white;
  background-color: black;
}

a:hover {
  color: black;
  background-color: white;
}

@media only screen and (max-width:992px) {
  .grid-container {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media only screen and (max-width: 747px) {
  .grid-container {
    grid-template-columns: repeat(1, 1fr);
  }
}

@media only screen and (max-width:576px) {
  .grid-container {
    padding-left: 1rem;
    padding-right: 1rem;
  }
}
</style>

<script>
export default {
  name: 'web-projects',
  data() {
    return {
      projects: [
        {name: 'Personal Website',desc:'My first project that utilizes a Front-end framework in development.'},
        {name: 'Photo Fetching Web', desc:'One of the projects from "The Creative JavaScript Course" by Dev Ed and Maxine Tillman.'}
      ],
      links: ['https://github.com/Tang2540/Personal-Web','https://github.com/Tang2540/Photon']
    };
  }
}
</script>