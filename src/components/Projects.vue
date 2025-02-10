<script setup>
import project1 from "@/assets/images/project1.jpg";
import project2 from "@/assets/images/project2.jpg";
import project3 from "@/assets/images/project3.jpg";

const projects = [
  {
    id: 1,
    title: "Portfolio Website",
    description: "Modern portfolio website with dark theme and smooth animations.",
    image: project1,
    technologies: ["Vue.js", "CSS", "HTML"],
    githubUrl: "https://github.com/username/project1",
    liveUrl: "https://project1.com",
  },
  {
    id: 2,
    title: "Social Media Website",
    description: "Social media website with to find out the best sport partners.",
    image: project2,
    technologies: ["Django", "Python", "PostgreSQL", "CSS", "HTML"],
    githubUrl: "https://github.com/zihong0526/fypteam",
    liveUrl: "https://project2.com",
  },
  {
    id: 3,
    title: "E-commerce Website",
    description: "A full-stack e-commerce solution with real-time inventory management.",
    image: project3,
    technologies: [
      "Wordpress",
      "WooCommerce",
      "Elementor",
      "Elementor Pro",
      "Plesk",
      "Webnic",
      "cpanel",
    ],
    githubUrl: "https://github.com/username/project3",
    liveUrl: "https://noura.com.sg",
  },
];
</script>

<template>
  <section class="projects-section" id="projects">
    <div class="section-header">
      <h2>Projects</h2>
      <p>Check out some of my recent work</p>
    </div>

    <div class="projects-container">
      <article v-for="project in projects" :key="project.id" class="project-card">
        <div class="project-image">
          <img :src="project.image" :alt="project.title" />
          <div class="project-links">
            <a :href="project.liveUrl" target="_blank" class="project-link live">
              <i class="fas fa-external-link-alt"></i>
              Live Demo
            </a>
            <a :href="project.githubUrl" target="_blank" class="project-link github">
              <i class="fab fa-github"></i>
              View Code
            </a>
          </div>
        </div>

        <div class="project-content">
          <h3 class="project-title">{{ project.title }}</h3>
          <p class="project-description">{{ project.description }}</p>

          <div class="project-tech">
            <span v-for="tech in project.technologies" :key="tech" class="tech-tag">
              {{ tech }}
            </span>
          </div>
        </div>
      </article>
    </div>
  </section>
</template>

<style scoped>
.projects-section {
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

.section-header h2 {
  font-size: 2rem;
  color: var(--primary-color);
  margin-bottom: 1rem;
}

.section-header p {
  color: #888;
}

.projects-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

.project-card {
  background: rgba(255, 255, 255, 0.05);
  border-radius: 20px;
  overflow: hidden;
  transition: transform 0.3s ease;
}

.project-card:hover {
  transform: translateY(-5px);
}

.project-image {
  position: relative;
  width: 100%;
  height: 200px;
  overflow: hidden;
}

.project-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.project-card:hover .project-image img {
  transform: scale(1.05);
}

.project-links {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.project-card:hover .project-links {
  opacity: 1;
}

.project-link {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.8rem 1.2rem;
  border-radius: 25px;
  text-decoration: none;
  font-size: 0.9rem;
  transition: transform 0.3s ease;
}

.project-link.live {
  background: var(--primary-color);
  color: var(--bg-color);
}

.project-link.github {
  background: rgba(255, 255, 255, 0.1);
  color: #fff;
}

.project-link:hover {
  transform: translateY(-3px);
}

.project-content {
  padding: 1.5rem;
}

.project-title {
  font-size: 1.3rem;
  color: #fff;
  margin-bottom: 1rem;
}

.project-description {
  color: #888;
  font-size: 0.95rem;
  line-height: 1.6;
  margin-bottom: 1rem;
}

.project-tech {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tech-tag {
  background: rgba(0, 255, 221, 0.1);
  color: var(--primary-color);
  padding: 0.4rem 0.8rem;
  border-radius: 15px;
  font-size: 0.8rem;
}

@media (max-width: 768px) {
  .projects-container {
    grid-template-columns: 1fr;
  }

  .project-links {
    opacity: 1;
    background: rgba(0, 0, 0, 0.7);
  }

  .project-link {
    padding: 0.6rem 1rem;
    font-size: 0.8rem;
  }
}
</style>
