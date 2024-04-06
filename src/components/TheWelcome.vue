<script setup>
import WelcomeItem from "./WelcomeItem.vue";
import { RouterLink } from "vue-router";
import DocumentationIcon from "./icons/IconDocumentation.vue";
import ToolingIcon from "./icons/IconTooling.vue";
import EcosystemIcon from "./icons/IconEcosystem.vue";
import CommunityIcon from "./icons/IconCommunity.vue";
import SupportIcon from "./icons/IconSupport.vue";
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Curriculum</template>

    Clicking
    <a href="./src/assets/cv/cv_zecamagalhaes.pdf" download>here</a>
    you will download my curriculum.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Professional Summary</template>

    Clicking
    <RouterLink to="/summary">here</RouterLink>
    you will be redirected to my professional summary.

    <br />

    You can see my certifications here:
    <RouterLink to="/certificates">Certificates</RouterLink>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Selected Projects</template>

    If you want to see some of my projects, you may
    <RouterLink to="/projects">click here</RouterLink>

    to get more information about them.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Languages Knowledge</template>

    <p>
      <a href="https://www.w3.org/html/" target="_blank" rel="noopener"
        ><strong>HTML</strong></a
      >
      <a
        href="https://www.w3.org/Style/CSS/Overview.en.html"
        target="_blank"
        rel="noopener"
        ><strong>CSS:</strong></a
      >
      Web content structuring and style.
    </p>

    <p>
      Dynamic web interactions ->
      <a
        href="https://developer.mozilla.org/en-US/docs/Web/JavaScript"
        target="_blank"
        rel="noopener"
        ><strong>JavaScript</strong></a
      >
    </p>

    <p>
      For interface development and animation,
      <a href="https://reactjs.org/" target="_blank" rel="noopener"
        ><strong>React</strong></a
      >
    </p>

    <p>
      <a href="https://vuejs.org/" target="_blank" rel="noopener"
        ><strong>Vue</strong></a
      >
      For interactive web interfaces.
    </p>

    <p>
      To enhance JavaScript reliability,
      <a href="https://www.typescriptlang.org/" target="_blank" rel="noopener"
        ><strong>TypeScript</strong></a
      >
      is the one.
    </p>

    <p>
      <a href="https://www.python.org/" target="_blank" rel="noopener"
        ><strong>Python:</strong></a
      >
      Web development and data analysis.
    </p>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Social</template>

    <p>
      Where you can find my code and projects on
      <a href="https://github.com/soutoux" target="_blank" rel="noopener"
        >GitHub</a
      >
      and
      <a
        href="https://www.linkedin.com/in/zeca-magalhães-9a67621a5/"
        target="_blank"
        rel="noopener"
        >LinkedIn</a
      >.
    </p>
  </WelcomeItem>
</template>
