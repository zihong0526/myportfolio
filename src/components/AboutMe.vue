<script setup>
const terminalLines = [
  { prefix: "$", text: "Hello!" },
  { prefix: ">", text: "I'm Zi Hong, and I specialize in web development from Malaysia." },
  {
    prefix: ">",
    text: "I'm a full-stack developer who loves creating elegant solutions to complex problems.",
  },
  {
    prefix: ">",
    text: "When I'm not coding, I enjoy reading, drawing, basketball, and gym.",
  },
  { prefix: "$", text: "cat skills.txt" },
  { prefix: ">", text: "• Frontend: Vue.js, React, TypeScript, CSS" },
  { prefix: ">", text: "• Backend: Django, Node.js, Python, PostgreSQL" },
  { prefix: ">", text: "• Tools: CloudFlare, Plesk, GitHub" },
];
</script>

<template>
  <section class="about-section" id="about">
    <div class="section-header">
      <h2>About Me</h2>
    </div>

    <div class="terminal-container">
      <div class="terminal-header">
        <div class="terminal-buttons">
          <span class="button close"></span>
          <span class="button minimize"></span>
          <span class="button maximize"></span>
        </div>
        <div class="terminal-title">about.txt</div>
      </div>

      <div class="terminal-content">
        <div v-for="(line, index) in terminalLines" :key="index" class="terminal-line">
          <span class="prefix">{{ line.prefix }}</span>
          <span class="text">{{ line.text }}</span>
        </div>
        <div class="terminal-line cursor">
          <span class="prefix">$</span>
          <span class="cursor-blink">█</span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  padding: 5rem 0;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.section-header {
  margin-bottom: 3rem;
}

.section-header h2 {
  font-size: 2rem;
  color: var(--primary-color);
  position: relative;
  display: inline-block;
  padding: 0.5rem 1rem;
  background: rgba(0, 255, 221, 0.1);
  border-radius: 8px;
}

.terminal-container {
  background: #1d1f21;
  border-radius: 10px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
  overflow: hidden;
  width: 100%;
  max-width: 800px;
  margin: 0 auto;
}

.terminal-header {
  background: #2d2d2d;
  padding: 0.8rem;
  display: flex;
  align-items: center;
}

.terminal-buttons {
  display: flex;
  gap: 0.5rem;
}

.button {
  width: 12px;
  height: 12px;
  border-radius: 50%;
}

.close {
  background: #ff5f56;
}

.minimize {
  background: #ffbd2e;
}

.maximize {
  background: #27c93f;
}

.terminal-title {
  color: #999;
  font-size: 0.9rem;
  margin-left: 1rem;
}

.terminal-content {
  padding: 1.5rem;
  font-family: "Fira Code", monospace;
  font-size: 0.9rem;
  line-height: 1.6;
}

.terminal-line {
  margin-bottom: 0.5rem;
  display: flex;
  gap: 1rem;
}

.prefix {
  color: var(--primary-color);
  user-select: none;
}

.text {
  color: #fff;
}

.cursor-blink {
  animation: blink 1s step-end infinite;
  color: var(--primary-color);
}

@keyframes blink {
  0%,
  100% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
}

@media (max-width: 768px) {
  .terminal-container {
    margin: 0 1rem;
  }

  .terminal-content {
    font-size: 0.8rem;
  }
}
</style>
