<template>
  <div class="certificates">
    <h1>My Certificates</h1>
    <div class="item">
      <div class="text-content" :class="'left-align'">
        <h2>Origamid</h2>
        <p>HTML & CSS for Beginners</p>
        <p>march/2024</p>
      </div>
      <div class="image-container">
        <a
          href="./src/assets/certificates/origamid_html-and-css-for-beginners-46h.pdf"
          target="_blank"
        >
          <img
            src="https://media.discordapp.net/attachments/852247434104274945/1226219055741141104/image.png?ex=6623f87c&is=6611837c&hm=50b6ccffd165a95fc1ddb6a6a37ead6d08e6625bd14a696d3e25ba72d4342e83&=&format=webp"
            alt="Certificate"
          />
        </a>
      </div>
    </div>

    <div class="item">
      <div class="text-content" :class="'right-align'">
        <h2>Origamid</h2>
        <p>CSS Grid Layout</p>
        <p>march/2024</p>
      </div>
      <div class="image-container">
        <a
          href="./src/assets/certificates/origamid_css-grid-layout-10h.pdf"
          target="_blank"
        >
          <img
            src="https://media.discordapp.net/attachments/852247434104274945/1226224066235596800/image.png?ex=6623fd27&is=66118827&hm=578b8418602f13f146fc983db9c39a536ff39d13f334363e3b8e1f29d491d10b&=&format=webp"
            alt="Certificate"
          />
        </a>
      </div>
    </div>

    <div class="item">
      <div class="text-content" :class="'left-align'">
        <h2>Origamid</h2>
        <p>CSS Flexbox</p>
        <p>march/2024</p>
      </div>
      <div class="image-container">
        <a
          href="./src/assets/certificates/origamid_css-flexbox-6h.pdf"
          target="_blank"
        >
          <img
            src="https://media.discordapp.net/attachments/852247434104274945/1226223911839207474/image.png?ex=6623fd02&is=66118802&hm=0dadd83cb8d7609677a7ae52b80c9c6c777f213d4c94d68d5f718462e05b8e3c&=&format=webp"
            alt="Certificate"
          />
        </a>
      </div>
    </div>
  </div>
</template>

<style>
.certificates {
  margin: 20px;
  height: 90vh;
  overflow-y: auto;
  padding-right: 30px;
  scrollbar-width: none;
  -ms-overflow-style: none;
}

.certificates::-webkit-scrollbar {
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

.image-container a:hover {
  background-color: #ffffff00;
}

.text-content {
  grid-area: text;
}
</style>
