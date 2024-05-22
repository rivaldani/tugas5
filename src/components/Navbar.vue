<template>
  <nav class="navbar">
    <div class="logo">Iphone Cell</div>
    <ul>
      <li>
        <a href="#home" title="Kembali ke halaman utama">Beranda</a>
      </li>
      <li>
        <a href="#products" title="Lihat produk kami">Produk</a>
      </li>
      <li>
        <a href="#about" title="Pelajari lebih lanjut tentang kami">Tentang Kami</a>
      </li>
      <li>
        <a href="#contact" title="Hubungi kami untuk informasi lebih lanjut">Kontak</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 50px;
  background-color: #75852e;
  color: white;
  border-bottom: 2px solid #004494; /* Tambahkan border bawah */
}

.navbar .logo {
  font-size: 28px; /* Lebih besar */
  font-weight: bold;
  text-transform: uppercase; /* Huruf kapital */
  letter-spacing: 2px; /* Spasi antar huruf */
}

.navbar ul {
  list-style: none;
  display: flex;
  margin: 0;
  padding: 0;
}

.navbar ul li {
  margin-left: 30px; /* Lebih banyak spasi antara item menu */
}

.navbar ul li a {
  color: rgb(117, 187, 70);
  text-decoration: none;
  font-size: 20px; /* Lebih besar */
  padding: 10px 15px; /* Lebih banyak ruang di dalam link */
  transition: background-color 0.3s ease; /* Efek transisi */
}

.navbar ul li a:hover {
  background-color: #004494;
  border-radius: 5px;
}
</style>
