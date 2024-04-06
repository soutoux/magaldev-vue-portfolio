<template>
  <div class="projects">
    <h1>Selected Projects</h1>
    <div class="item" v-for="n in 4" :key="n">
      <div
        class="text-content"
        :class="{ 'left-align': n % 2 !== 0, 'right-align': n % 2 === 0 }"
      >
        <h2>Project {{ n }}</h2>
        <p>Description for Project {{ n }}</p>
      </div>
      <div class="image-container">
        <img
          src="https://via.placeholder.com/400x300.png?text=Projects Image"
          alt="Project {{ n }} image"
        />
        <div class="overlay">
          <button class="btn preview">Preview</button>
          <button class="btn source">Source</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.projects {
  margin: 20px;
  height: 90vh;
  overflow-y: auto;
  padding-right: 30px;
  scrollbar-width: none;
  -ms-overflow-style: none;
}

.projects::-webkit-scrollbar {
  display: none;
}

.item {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  margin-bottom: 20px;
  gap: 20px;
}

.item:nth-child(odd) {
  grid-template-areas: "text image";
}

.item:nth-child(even) {
  grid-template-areas: "image text";
}

.left-align {
  text-align: left;
}

.right-align {
  text-align: right;
}

.image-container {
  position: relative;
  grid-area: image;
}

.image-container img {
  max-width: 400px;
  border-radius: 4px;
  display: block;
  width: 100%;
}

.text-content {
  grid-area: text;
}

.overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: space-around;
  align-items: center;
  opacity: 0;
  transition: opacity 0.3s;
  background: rgba(0, 0, 0, 0.5);
}

.image-container:hover .overlay {
  opacity: 1;
}

.btn {
  width: 50%;
  height: 40px;
  padding: 0;
  margin: 0;
  color: white;
  border: none;
  cursor: pointer;
  text-align: center;
  background-color: transparent;
  transition: 0.4s;
}

.preview {
  background-color: #28a745;
  border-radius: 0 0 0 4px;
}

.source {
  background-color: #218838;
  border-radius: 0 0 4px 0;
}

.preview:hover {
  background-color: #218836c2;
}

.source:hover {
  background-color: #28a746c2;
}
</style>
