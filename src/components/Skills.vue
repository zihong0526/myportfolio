<script setup>
const skills = {
  webDevelopment: [
    { name: "HTML", icon: "html5", color: "#E44D26" },
    { name: "CSS", icon: "css3", color: "#1572B6" },
    { name: "React", icon: "react", color: "#61DAFB" },
    { name: "Vue", icon: "vuejs", color: "#4FC08D" },
    { name: "Node.js", icon: "node-js", color: "#339933" },
    { name: "Django", icon: "python", color: "#fcba03" },
  ],
  programmingLanguages: [
    { name: "C++", icon: "cuttlefish", color: "#00599C" },
    { name: "Java", icon: "java", color: "#007396" },
    { name: "Python", icon: "python", color: "#3776AB" },
    { name: "JavaScript", icon: "js", color: "#3776AB" },
  ],
};
</script>

<template>
  <section class="skills-section" id="skills">
    <div class="section-header">
      <div class="code-icon">&lt;/&gt;</div>
      <h2>Skills</h2>
      <p>I'm enjoying to learn new things and creating</p>
    </div>

    <div class="skills-container">
      <div class="skill-category">
        <div class="category-header">
          <div class="category-badge">Web Development</div>
          <span class="category-subtitle">Full Stack Web Dev</span>
        </div>
        <div class="skills-grid">
          <div
            v-for="skill in skills.webDevelopment"
            :key="skill.name"
            class="skill-item"
            :style="{ '--skill-color': skill.color }"
          >
            <div class="skill-icon">
              <i v-if="skill.icon !== 'cuttlefish'" :class="`fab fa-${skill.icon}`"></i>
              <span v-else class="cpp-text">C++</span>
            </div>
            <span class="skill-name">{{ skill.name }}</span>
          </div>
        </div>
      </div>

      <div class="skill-category mt-4">
        <div class="category-header">
          <div class="category-badge">Programming Languages</div>
          <span class="category-subtitle">Core Languages</span>
        </div>
        <div class="skills-grid">
          <div
            v-for="skill in skills.programmingLanguages"
            :key="skill.name"
            class="skill-item"
            :style="{ '--skill-color': skill.color }"
          >
            <div class="skill-icon">
              <i :class="`fab fa-${skill.icon}`"></i>
            </div>
            <span class="skill-name">{{ skill.name }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.skills-section {
  padding: 5rem 0;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.section-header {
  text-align: center;
  margin-bottom: 4rem;
}

.code-icon {
  font-size: 3rem;
  color: var(--primary-color);
  margin-bottom: 1rem;
}

.section-header h2 {
  font-size: 3rem;
  color: var(--primary-color);
  margin-bottom: 1rem;
}

.section-header p {
  color: #888;
  font-size: 1.1rem;
}

.skills-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.skill-category {
  background: rgba(22, 28, 36, 0.8);
  border-radius: 24px;
  padding: 3rem;
}

.category-header {
  margin-bottom: 3rem;
}

.category-badge {
  display: inline-block;
  background: rgba(0, 255, 221, 0.1);
  color: var(--primary-color);
  padding: 0.8rem 1.5rem;
  border-radius: 20px;
  font-size: 1.1rem;
  margin-bottom: 0.8rem;
}

.category-subtitle {
  color: #888;
  font-size: 1rem;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  gap: 3rem;
}

.skill-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  transition: transform 0.3s ease;
}

.skill-item:hover {
  transform: translateY(-8px);
}

.skill-icon {
  width: 100px;
  height: 100px;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 16px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 3rem;
  color: var(--skill-color);
  transition: all 0.3s ease;
}

.skill-item:hover .skill-icon {
  background: var(--skill-color);
  color: white;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
}

.skill-name {
  font-size: 1rem;
  color: #fff;
  font-weight: 500;
}

.cpp-text {
  font-size: 2rem;
  font-weight: bold;
  font-family: monospace;
}

@media (max-width: 1200px) {
  .skills-grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
  }
}

@media (max-width: 768px) {
  .skills-container {
    padding: 0 1rem;
  }

  .skill-category {
    padding: 2rem;
  }

  .skills-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }

  .skill-icon {
    width: 80px;
    height: 80px;
    font-size: 2.5rem;
  }

  .section-header h2 {
    font-size: 2.5rem;
  }
}

@media (max-width: 480px) {
  .skills-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
  }

  .skill-icon {
    width: 70px;
    height: 70px;
    font-size: 2rem;
  }

  .skill-name {
    font-size: 0.9rem;
  }
}
</style>
