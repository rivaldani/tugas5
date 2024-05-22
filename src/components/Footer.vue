<template>
  <nav class="navbar">
    <div class="logo">Iphone Cell</div>
    <ul class="nav-links">
      <li><a href="#home">Beranda</a></li>
      <li><a href="#products">Produk</a></li>
      <li><a href="#about">Tentang Kami</a></li>
      <li><a href="#contact">Kontak</a></li>
    </ul>
    <div class="burger" @click="toggleNav()">
      <div class="line1"></div>
      <div class="line2"></div>
      <div class="line3"></div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    toggleNav() {
      this.isOpen = !this.isOpen;
    }
  }
}
</script>

<style scoped>
.navbar {
  background-color: #b39200;
  color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 30px;
}

.logo {
  font-size: 24px;
  font-weight: bold;
}

.nav-links {
  display: flex;
  justify-content: space-around;
  align-items: center;
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.nav-links li {
  margin: 0 15px;
}

.nav-links li a {
  color: white;
  text-decoration: none;
  font-size: 18px;
  transition: color 0.3s ease;
}

.nav-links li a:hover {
  color: #ce2406;
}

.burger {
  display: none;
  cursor: pointer;
}

.burger div {
  width: 25px;
  height: 3px;
  background-color: white;
  margin: 5px;
  transition: all 0.3s ease;
}

@media screen and (max-width: 768px) {
  .nav-links {
    display: none;
  }

  .burger {
    display: block;
  }

  .navbar.active .nav-links {
    display: flex;
    flex-direction: column;
    position: absolute;
    top: 70px;
    background-color: #c41212;
    width: 100%;
    left: 0;
    text-align: center;
    z-index: 1;
  }

  .navbar.active .nav-links li {
    margin: 15px 0;
  }

  .navbar.active .burger .line1 {
    transform: rotate(-45deg) translate(-5px, 6px);
  }

  .navbar.active .burger .line2 {
    opacity: 0;
  }

  .navbar.active .burger .line3 {
    transform: rotate(45deg) translate(-5px, -6px);
  }
}
</style>
