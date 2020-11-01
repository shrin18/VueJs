<template>
  <nav>
    <div class="menu-item"><a href="#">Home</a></div>
    <div class="menu-item"><a href="#">About</a></div>
    <Dropdown title="Services" :items="services" />
    <div class="menu-item"><a href="#">Contact</a></div>
  </nav>
</template>

<script>
import Dropdown from './Dropdown';

export default {
  name: 'navbar',
  components: {
    Dropdown
  },
  data () {
    return {
      services: [
        {
          title: 'Web',
          link: 'www.google.com'
        },
        {
          title: 'Design',
          link:'#'
        },
        {
          title: 'Videos',
          link: '#'
        }
      ]
    }
  }
}
</script>

<style>
nav {
  display: flex;
  align-items: center;
  justify-content: center;
}

nav .menu-item {
  color: #FFF;
  padding: 50px 30px;
  position: relative;
  text-align: center;
  border-bottom: 7px solid transparent;
  display: flex;
  transition: 0.4s;
}

nav .menu-item.active,
nav .menu-item:hover {
  background-color: #444;
  border-bottom-color: #FF5858;
}

nav .menu-item a {
  color: inherit;
  text-decoration: none;
}
</style>