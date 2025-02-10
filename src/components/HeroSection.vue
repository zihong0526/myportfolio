<script setup>
import profileImage from "@/assets/images/photo.jpg";
</script>

<template>
  <section class="hero" id="home">
    <div class="hero-container">
      <!-- Left side - Profile Card -->
      <div class="hero-card">
        <div class="profile-image">
          <img :src="profileImage" alt="Profile" />
        </div>

        <h2 class="name">Zi Hong</h2>
        <h3 class="title">Full-stack developer</h3>

        <div class="contact-info">
          <div class="info-item">
            <span class="material-symbols-outlined">mail</span>
            <span>pangzihong2@gmail.com</span>
          </div>
          <div class="info-item">
            <span class="material-symbols-outlined">location_on</span>
            <span>Malaysian</span>
          </div>
          <div class="info-item">
            <span class="material-symbols-outlined">work</span>
            <span>Fresh Graduate</span>
          </div>
          <div class="info-item">
            <span class="material-symbols-outlined">language</span>
            <a href="https://www.linkedin.com/in/pang-zi-hong-5577761b7/">Linkedin</a>
          </div>
        </div>

        <div class="skills">
          <span class="skill-tag">HTML</span>
          <span class="skill-tag">CSS</span>
          <span class="skill-tag">JS</span>
          <span class="skill-tag">REACT</span>
        </div>

        <a href="/resume.pdf" class="download-btn" download>
          Download CV <span class="material-symbols-outlined">download</span>
        </a>
      </div>

      <!-- Center - Text Content -->
      <div class="hero-content">
        <div class="content-wrapper">
          <h1 class="main-title">
            <span class="title-tag">&lt;h1&gt;</span>
            Hey<br />
            I'm <span class="highlight">ZiHong</span>,<br />
            Full-Stack<br />
            Developer
            <span class="title-tag">&lt;/h1&gt;</span>
          </h1>

          <p class="description">
            <span class="title-tag">&lt;p&gt;</span>
            Hello, I'm a fresh IT graduate skilled in full-stack development, specializing in
            frontend (HTML, CSS, JavaScript, Vue, React) and backend (Django, SQL). Open to job
            opportunities in software development and IT roles. Let's connect!
            <span class="title-tag">&lt;/p&gt;</span>
          </p>

          <a href="#contact" class="talk-btn"> Let's Talk <i class="fas fa-envelope"></i> </a>
        </div>
      </div>

      <!-- Right side - Stats -->
      <div class="stats">
        <div class="stat-item">
          <span class="stat-number">4</span>
          <span class="stat-label">Programming Language</span>
        </div>
        <div class="stat-item">
          <span class="stat-number">6</span>
          <span class="stat-label">Development Tools</span>
        </div>
        <div class="stat-item">
          <span class="stat-number">1</span>
          <span class="stat-label">Years of Experience</span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  padding: 2rem;
}

.hero-container {
  max-width: 1400px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: minmax(350px, 400px) 1fr 250px;
  gap: 4rem;
  align-items: center;
  width: 100%;
}

.hero-card {
  background: var(--bg-color);
  border-radius: 30px;
  padding: 3rem;
  width: 100%;
  max-width: 400px;
  text-align: center;
  position: relative;
  border: 1px solid rgba(255, 255, 255, 0.1);
  overflow: hidden;
}

.hero-card::before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 100%;
  height: 100%;
  background: var(--primary-color);
  clip-path: circle(180px at 80% 20%);
  opacity: 0.1;
}

.profile-image {
  width: 120px;
  height: 120px;
  margin: 0 auto 1.5rem;
  border-radius: 50%;
  overflow: hidden;
  border: 3px solid var(--primary-color);
}

.profile-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.name {
  font-size: 2rem;
  margin-bottom: 0.5rem;
  color: var(--text-color);
}

.title {
  font-size: 1.2rem;
  color: var(--primary-color);
  margin-bottom: 2rem;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-bottom: 2rem;
}

.info-item {
  display: flex;
  align-items: center;
  gap: 0.8rem;
  color: #888;
}

.info-item .material-symbols-outlined {
  color: var(--primary-color);
  font-size: 20px;
}

.skills {
  display: flex;
  gap: 0.8rem;
  justify-content: center;
  flex-wrap: wrap;
  margin-bottom: 2rem;
}

.skill-tag {
  background: rgba(0, 255, 221, 0.1);
  color: var(--primary-color);
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.9rem;
}

.download-btn {
  background: #fff;
  color: var(--bg-color);
  padding: 0.8rem 2rem;
  border-radius: 25px;
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-weight: 500;
  transition: transform 0.3s ease;
}

.download-btn:hover {
  transform: translateY(-3px);
}

/* New content styles */
.hero-content {
  padding: 2rem 0;
}

.content-wrapper {
  max-width: 600px;
}

.main-title {
  font-size: 4.5rem;
  line-height: 1.1;
  margin-bottom: 2rem;
  position: relative;
}

.highlight {
  color: var(--primary-color);
}

.title-tag {
  color: var(--primary-color);
  opacity: 0.5;
  font-size: 1rem;
  font-family: monospace;
}

.description {
  font-size: 1.2rem;
  color: #888;
  margin-bottom: 2rem;
  line-height: 1.6;
  max-width: 500px;
}

.talk-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  color: var(--primary-color);
  text-decoration: none;
  font-size: 1.2rem;
  transition: transform 0.3s ease;
}

.talk-btn:hover {
  transform: translateY(-3px);
}

/* Stats styles */
.stats {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  background: rgba(255, 255, 255, 0.05);
  padding: 2rem;
  border-radius: 20px;
  height: fit-content;
}

.stat-item {
  text-align: left;
}

.stat-number {
  color: var(--primary-color);
  font-size: 2.5rem;
  font-weight: bold;
  display: block;
}

.stat-label {
  color: #888;
  font-size: 0.9rem;
}

@media (max-width: 1400px) {
  .hero-container {
    grid-template-columns: minmax(300px, 350px) 1fr;
    gap: 3rem;
  }

  .stats {
    grid-column: 2;
    flex-direction: row;
    justify-content: flex-start;
    margin-top: 2rem;
  }

  .stat-item {
    flex: 1;
  }
}

@media (max-width: 1024px) {
  .hero-container {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .hero-card {
    margin: 0 auto;
  }

  .hero-content {
    text-align: center;
  }

  .content-wrapper {
    margin: 0 auto;
  }

  .description {
    margin-left: auto;
    margin-right: auto;
  }

  .stats {
    grid-column: 1;
    justify-content: center;
  }
}

@media (max-width: 768px) {
  .main-title {
    font-size: 3.5rem;
  }

  .stats {
    flex-wrap: wrap;
    gap: 1.5rem;
  }

  .stat-item {
    flex: 1 1 calc(33% - 1rem);
    text-align: center;
  }
}

@media (max-width: 480px) {
  .hero {
    padding: 1rem;
  }

  .main-title {
    font-size: 2.5rem;
  }

  .description {
    font-size: 1rem;
  }

  .stats {
    padding: 1.5rem;
  }

  .stat-number {
    font-size: 2rem;
  }

  .stat-label {
    font-size: 0.8rem;
  }
}
</style>
