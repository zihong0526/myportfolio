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
    githubUrl: "https://github.com/zihong0526/myportfolio",
    liveUrl: "https://myportfoliozh.netlify.app/",
  },
  {
    id: 2,
    title: "Social Media Website",
    description: "Social media website with to find out the best sport partners.",
    image: project2,
    technologies: ["Django", "Python", "PostgreSQL", "CSS", "HTML"],
    githubUrl: "https://github.com/zihong0526/fypteam",
    liveUrl: "",
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
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-5 h-5"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M13.5 6H5.25A2.25 2.25 0 0 0 3 8.25v10.5A2.25 2.25 0 0 0 5.25 21h10.5A2.25 2.25 0 0 0 18 18.75V10.5m-10.5 6L21 3m0 0h-5.25M21 3v5.25"
                />
              </svg>
              Live Demo
            </a>
            <a
              v-if="project.githubUrl"
              :href="project.githubUrl"
              target="_blank"
              class="project-link github"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="w-5 h-5"
                viewBox="0 0 24 24"
                fill="currentColor"
              >
                <path
                  d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"
                />
              </svg>
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
