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
      <h2>discover our collection</h2>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        { src: "/images/5.jpg", alt: "Open book with artwork" },
        { src: "/images/5.jpg", alt: "Black and white photo book" },
        { src: "/images/5.jpg", alt: "Open book with text" },
        { src: "/images/5.jpg", alt: "Close-up of text in book" },
        { src: "/images/5.jpg", alt: "Orange book cover" },
        { src: "/images/5.jpg", alt: "Black box book - FEDRIGONI" },
        { src: "/images/book7.jpg", alt: "Book with digital art" },
        { src: "/images/book8.jpg", alt: "Uncoated colors book" },
        { src: "/images/book9.jpg", alt: "Typography book with 'Hi'" },
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
