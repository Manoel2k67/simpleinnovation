<template>
  <header>
    <nav>
      <ul>
        <div class="logo">LOGO</div>
        <div class="menu-items">
          <li><a>INICIO</a></li>
          <li><a>QUEM SOMOS?</a></li>
          <li><a>NOSSOS PROJETOS</a></li>
          <li><a>CONTATO --></a></li>
        </div>
      </ul>
    </nav>
  </header>
</template>

<script setup lang="ts">
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:ital,wght@0,100..800;1,100..800&display=swap');

header {
  padding: 0.3rem;

}

nav ul {
  list-style: none;
  padding: 0;
  display: flex;
  align-items: center;
  font-family: 'JetBrains Mono', monospace;
  width: 100%;
}

.logo {
  font-weight: bold;
  font-size: 14px;
  margin-left: 143px;
  margin-right: 71px;
  color: #0C0A09;
}

.menu-items {
  display: flex;
  margin-left: auto;
}

nav ul div {
    font-weight: bold;
    font-size: 14px;
    margin-left: 143px;
    margin-right: 71px;
    color: #0C0A09;
}

nav ul li {
  display: inline;
  margin-right: 31px;
}


nav ul li a:hover {
  border-bottom: 5px solid #0C0A09;
}

nav ul li:last-child a {
  background-color: #F97316;
  color: #fff;
  font-weight: bold;
  padding: 15px 24px;
  border-bottom: none;
}

nav ul li:last-child a:hover {
  background-color: #f95e16;
  text-decoration: underline;
  border-bottom: none;
  cursor: pointer;
}

nav ul li a {
  cursor: pointer;
  color: #0C0A09;
  text-decoration: none;
}









@media (min-width: 768px) and (max-width: 1024px) {

  .menu-items{
    display: flex;
    justify-content: center;
    align-items: start;
    
  }

  .logo {
    font-size: 1rem;
  }

  nav ul li {
    margin-right: 15px;
    font-size: 0.8rem;
  }

  nav ul li:last-child a {
    padding: 10px 15px;
    font-size: 0.8rem;
  }

}


</style>
