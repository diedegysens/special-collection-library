<template>
    <div class="container">
      <!-- Header -->
      <header class="header">
        <h1 class="logo">sint<br />— lukas<br />bibliotheek</h1>
        <nav class="nav">
          <a href="#" class="nav-link">menu</a>
          <a href="#" class="nav-link">search</a>
        </nav>
      </header>
  
      <!-- Image Grid -->
      <section class="grid">
        <div v-for="(image, index) in images" :key="index" class="grid-item">
          <img :src="image.src" :alt="image.alt" />
        </div>
      </section>
  
      <!-- Title -->
      <div class="title">
        <div class="buttonBack font-bold">
        <NuxtLink to="/books">discover our collection</NuxtLink>
    </div>
      </div>
    </div>
    
  </template>
  
  <script>
  export default {
    data() {
      return {
        images: [
          { src: "/images/5 normaal.jpeg", alt: "Open book with artwork" },
          { src: "/images/8 normaal.jpeg", alt: "Black and white photo book" },
          { src: "/images/9 2 normaal.jpeg", alt: "Open book with text" },
          { src: "/images/9 3 normaal.jpeg", alt: "Close-up of text in book" },
          { src: "/images/9 4 normaal.jpeg", alt: "Orange book cover" },
          { src: "/images/9 5 normaal.jpeg", alt: "Black box book - FEDRIGONI" },
          { src: "/images/9 normaal.jpeg", alt: "Book with digital art" },
          { src: "/images/11 normaal.jpeg", alt: "Uncoated colors book" },
          { src: "/images/12 2 normaal.jpeg", alt: "Typography book with 'Hi'" },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  /* Container */
  .container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 40px;
  }
  
  /* Header */
  .header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    font-family: serif;
    font-size: 20px;
  }
  
  .logo {
    font-weight: bold;
    text-transform: lowercase;
  }
  
  .nav {
    display: flex;
    gap: 20px;
  }
  
  .nav-link {
    text-decoration: none;
    color: black;
    font-size: 18px;
    font-weight: bold;
  }
  
  /* Grid */
  .grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
    margin-top: 20px;
  }
  
  .grid-item img {
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 5px;
  }
  
  /* Title */
  .title {
    margin-top: 40px;
    font-size: 48px;
    font-weight: bold;
    text-transform: lowercase;
  }
  </style>
  
   

