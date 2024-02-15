<template>
  <nav>
    <div class="logo" :style="{'color': isMenuOpen ? 'white' : 'black'}">P. Mapunya</div>
    <ul :class="{'show-menu':isMenuOpen}">
      <li><a href="#about">About</a></li>
      <li><a  href="#expertise">Specialties</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#certificates">Certificates</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    
    <div class="hamburger-icon" @click="toggleMenu">
      <span id="line2" :style="{'backgroundColor': isMenuOpen ? 'white' : 'black'}"></span>
      <span id="line3" :style="{'backgroundColor': isMenuOpen ? 'white' : 'black'}"></span>
      <span id="line1" :style="{'backgroundColor': isMenuOpen ? 'white' : 'black'}"></span>
    </div>
    <div class="cover" :style="{'visibility': isMenuOpen ? 'visible' : 'hidden','opacity':isMenuOpen?'1':'0'}"></div>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      isMenuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
      if(this.isMenuOpen){
      document.body.style.overflow = 'hidden';
      }else{
      document.body.style.overflow = 'auto';
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  nav {
    display: flex;
    background-color: white;
    justify-content: space-around;
    align-items: center;
    height: 17vh;
    position: fixed;
    width: 100vw;
    top: 0;
    left: 0;
    border-bottom:1px solid #d8e2ec;
    animation: slide-down 1s;
  }

  @keyframes slide-down {
    from {transform: translateY(-100%)}
    to {transform: translateY(0)}
  }

  .logo {
    font-size: 2rem;
    pointer-events: none;
    z-index: 1000;
  }

  ul {
    display: flex;
    list-style: none;
    font-size: 1.5rem;
    gap: 2rem;
    z-index: 1000;
  }

  a {
    color: black;
    text-decoration: none;
  }

  a:hover {
    color:darkgray
  }

  .hamburger-icon {
    display: none;
    z-index: 1000;
    position: relative;
  }

  .hamburger-icon span {
    width: 50px;
    height: 2px;
    z-index: 1000;
  }

  .cover {
    min-height: 100vh;
    position: fixed;
    background-color: black;
    min-width: 100vw;
    top: 0;
    left: 0;
    transition: all 0.3s ease;
    z-index: 999;
  }

  .show-menu {
    display: flex;
    flex-direction: column;
    position: absolute;
    transform: translate(0,75%);
  }

  @media only screen and (max-width:1024px) {
    a {
      font-size: 1.25rem;
    }
  }

  @media only screen and (max-width: 768px) {

    .hamburger-icon {
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
    }

    ul {
      display: none;
      font-size: 3rem;
      font-weight: 600;
    }

    a {
      color: white;
    }
  }

  @media only screen and (max-width:576px) {

    .hamburger-icon span {
      width: 25px;
    }
  }
</style>
