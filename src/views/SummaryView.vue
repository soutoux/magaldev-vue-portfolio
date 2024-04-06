<template>
  <div class="summary">
    <h1 class="title">Summary</h1>
    <p class="desc">
      Here is a summary of my professional experience. For each company, I've
      listed the functions I held and the dates I worked there.
    </p>

    <ol>
      <li>
        <strong>Senior Software Engineer at UngaBunga</strong><br />
        <span>June 2019 - Present</span>
      </li>
      <li>
        <strong>Software Engineer at LuiogaUn</strong><br />
        <span>April 2017 - June 2019</span>
      </li>
      <li>
        <strong>Software Engineer at LuiogaUn Labs</strong><br />
        <span>February 2016 - April 2017</span>
      </li>
      <li>
        <strong>Full Stack Developer at Ahuuog</strong><br />
        <span>September 2014 - February 2016</span>
      </li>
    </ol>

    <h1 class="title">Education</h1>
    <p class="desc">Below are the degrees I've obtained.</p>

    <ol>
      <li>
        <strong>Bachelor of Computer Science</strong><br />
        <span>Universidade Federal do Paraná, 2012 - 2014</span>
      </li>
      <li>
        <strong>Master of Computer Science</strong><br />
        <span>Universidade Federal do Paraná, 2015 - 2017</span>
      </li>
    </ol>
  </div>
</template>

<script></script>

<style>
.summary {
  margin: 20px;
  height: 90vh;
  overflow-y: auto;
  padding-right: 30px;
  scrollbar-width: none;
  -ms-overflow-style: none;
}

.summary::-webkit-scrollbar {
  display: none;
}

.title,
.desc {
  text-align: end;
}

.desc {
  margin-bottom: 2rem;
}

ol {
  counter-reset: chapter 0;
  list-style: none;
  margin: 0;
  padding: 0;
  text-align: center;
}

ol li {
  counter-increment: chapter;
  margin: 10px 0;
}

ol li::before {
  content: counters(chapter, ".") " - ";
  font-size: 0.8em;
  color: #999;
}
</style>
