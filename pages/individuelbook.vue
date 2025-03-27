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
  
      <!-- Book Details -->
      <section class="book-details">
        <div class="main-image">
          <img :src="book.cover" :alt="book.title" />
        </div>
        <div class="side-images">
          <img v-for="(image, index) in book.images" :key="index" :src="image" :alt="`Book image ${index + 1}`" />
        </div>
        <div class="book-info">
          <h2>book <span class="number">{{ book.number }}</span></h2>
          <span class="availability">available in library</span>
          <p class="description">{{ book.description }}</p>
        </div>
      </section>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        book: {
          number: "nr1",
          title: "Sheila Hicks",
          cover: "/images/9 4.jpg",
          images: [
            "/images/9.jpg",
            "/images/9 2.jpg",
            "/images/9 3.jpg",
          ],
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat...",
        },
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
  
  /* Book Details */
  .book-details {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 20px;
    margin-top: 20px;
  }
  
  /* Main Image */
  .main-image img {
    width: 100%;
    height: auto;
    border-radius: 5px;
  }
  
  /* Side Images */
  .side-images {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 10px;
  }
  
  .side-images img {
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 5px;
  }
  
  /* Book Info */
  .book-info {
    grid-column: span 2;
    margin-top: 20px;
  }
  
  h2 {
    font-size: 48px;
    font-weight: bold;
    text-transform: lowercase;
  }
  
  .number {
    font-size: 48px;
    font-weight: bold;
  }
  
  .availability {
    font-size: 18px;
    font-weight: normal;
    margin-left: 10px;
  }
  
  .description {
    margin-top: 20px;
    font-size: 16px;
    line-height: 1.5;
  }
  </style>
  