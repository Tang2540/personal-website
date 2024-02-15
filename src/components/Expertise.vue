<template>
    <div class="grid-container">
        <div class="content-container" v-for="(expertise,index) in expertise" :key="index">
            <div class="skill-name">{{ expertise.name }}</div>
            <ul v-for="(skill,index) in expertise.skills" :key="index">
                <li>{{ skill }}</li>
            </ul>
        </div>
    </div>
</template>

<style scoped>
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 3fr);
    grid-gap: 4rem;
    padding: 20px;
}

.skill-name {
    text-align: center;
    font-weight: 600;
}

@media only screen and (max-width: 785px) {
    .grid-container {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media only screen and (max-width: 576px) {
    .grid-container {
        grid-template-columns: repeat(1, 1fr);
        padding: 0;
    }
}
</style>

<script>
export default {
    name: 'web-expertise',
    data() {
    return {
      expertise: [
        {name: 'Programming and Scripting Languages', skills:['HTML','CSS','JavaScript','Python','SQL']},
        {name:'Front-end Tools',skills:['Vue.js','Bootstrap','GSAP']},
        {name:'Back-end Tools', skills:['Node.js','Express.js']},
        {name: 'Methodologies', skills:['Software Testing','SDLC']},
        {name:'Testing Tools',skills:['Selenium','Hoppscotch']},
        {name:'Cloud Service',skills:['Azure','AWS']}
      ]
    };
  }
}
</script>