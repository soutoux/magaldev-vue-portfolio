<template>
  <div class="about">
    <h1>About Me</h1>
    <p>
      Hello! I'm <span>Zeca Magalhães</span>, a Brazilian
      <span>Front-End</span> developer and <span>minimalist</span> designer. I
      specialize in HTML, CSS, JavaScript, React, Vue, Tailwind, Typescript and
      Python. Fluent in Portuguese, English, Spanish, and French, I bring a
      global perspective to my projects. I prioritize <span>usability</span> and
      <span>accessibility</span> in my designs, focusing on simplicity and
      organization. Outside of work, I'm passionate about football, military,
      and aviation, which keep me inspired. My goal is to create digital
      experiences that are not only visually appealing but also
      <span>intuitive</span> and <span>accessible for everyone</span>. Let's
      discuss how I can enhance your next project with creativity and
      <span>efficiency</span>.
    </p>
  </div>
</template>

<style>
.about {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0 2rem;
  text-align: center;
}

span {
  color: #00bd7e;
}

@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}

@media (max-width: 1000px) {
  .about {
    margin-top: 1rem;
  }
}
</style>
