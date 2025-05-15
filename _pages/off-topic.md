---
title: "off topic"
permalink: /off-topic/
layout: single
author_profile: true
---

<div class="notice--info" style="display: none;">
  <h4>Why Off Topic?</h4>
  <p>Adding a bit of human touch to this blog - because life isn't just about research and work!</p>
</div>

<div class="off-topic-grid">
  <!-- Column 1 -->
  <div class="grid-column">
    <div class="section-card">
      <h2>🎬 Movies</h2>
      <div class="movies-section">
        <div class="movie-list">
          1. Blade Runner (1982)
          2. La Strada (1954)
          3. Anatomy of a Fall (2023)
          4. Brokeback Mountain (2005)
          5. The Devil, Probably (1977)
          6. Casablanca (1942)
          7. The Great Gatsby (2013)
        </div>
        <div class="movie-actions">
          <a href="/off-topic/movies/" class="movie-thoughts-btn">Share Movie Thoughts</a>
        </div>
      </div>
    </div>

    <div class="section-card">
      <h2>🎵 Music</h2>
      <div id="spotify-player">
        <div class="spotify-mini">
          <iframe style="border-radius:4px" 
                  src="https://open.spotify.com/embed/track/2fRF1w5mM5ZIUvZvHswpdw?utm_source=generator" 
                  width="100%" 
                  height="80" 
                  frameBorder="0" 
                  allowfullscreen="" 
                  allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" 
                  loading="lazy">
          </iframe>
        </div>
      </div>
    </div>
  </div>

  <!-- Column 2 -->
  <div class="grid-column">
    <div class="section-card">
      <h2>🏃‍♂️ Sports</h2>
      <div class="sports-section">
        <a href="/off-topic/sports/" class="section-link">Read my sports thoughts and updates</a>
      </div>
    </div>

    <div class="section-card">
      <h2>💧 Water Intake</h2>
      <div id="water-tracker">
        <div class="water-stats">
          <div class="water-graph">
            <canvas id="waterChart"></canvas>
          </div>
          <div class="water-summary">
            <p>Last month: 1.5L/day</p>
            <p>Last 3 months: 1.2L/day</p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Column 3 -->
  <div class="grid-column">
    <div class="section-card">
      <h2>🌟 Language Learning</h2>
      <div class="duolingo-section">
        <p>Learning French on Duolingo! <a href="https://www.duolingo.com/profile/jyanqa" target="_blank">Follow my progress</a></p>
      </div>
    </div>
  </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
// Water tracking graph
const ctx = document.getElementById('waterChart').getContext('2d');
const waterChart = new Chart(ctx, {
  type: 'line',
  data: {
    labels: Array.from({length: 30}, (_, i) => `Day ${i + 1}`),
    datasets: [{
      label: 'Daily Water Intake (L)',
      data: Array.from({length: 30}, () => 1.2 + Math.random() * 0.6),
      borderColor: '#008080',
      tension: 0.4,
      fill: false
    }]
  },
  options: {
    responsive: true,
    maintainAspectRatio: false,
    plugins: {
      legend: {
        display: false
      }
    },
    scales: {
      y: {
        beginAtZero: true,
        max: 2.5,
        title: {
          display: true,
          text: 'Liters'
        }
      }
    }
  }
});
</script>

<style>
.off-topic-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  margin: 20px 0;
}

.grid-column {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.section-card {
  background-color: #f8f9fa;
  padding: 15px;
  border-radius: 8px;
  height: 100%;
}

.section-card h2 {
  color: #008080;
  margin-top: 0;
  margin-bottom: 15px;
  font-size: 1.2em;
}

.water-stats {
  padding: 0;
}

.water-graph {
  height: 150px;
  margin: 10px 0;
}

.water-summary {
  font-size: 0.85em;
  color: #666;
  margin-top: 10px;
}

.spotify-mini {
  max-width: 100%;
  margin: 0;
}

.duolingo-section {
  background-color: transparent;
  padding: 0;
  margin: 0;
  font-size: 0.9em;
}

.duolingo-section a {
  color: #008080;
  text-decoration: underline;
}

.duolingo-section a:hover {
  color: #006666;
}

.movies-section {
  margin: 0;
}

.movie-list {
  margin-bottom: 10px;
  font-size: 0.9em;
}

.movie-actions {
  margin-top: 10px;
}

.movie-thoughts-btn {
  display: inline-block;
  background-color: #008080;
  color: white;
  padding: 6px 12px;
  border-radius: 4px;
  text-decoration: none;
  font-size: 0.85em;
  transition: background-color 0.3s;
}

.movie-thoughts-btn:hover {
  background-color: #006666;
  color: white;
  text-decoration: none;
}

.section-link {
  color: #008080;
  text-decoration: none;
  display: block;
  padding: 6px 0;
}

.section-link:hover {
  color: #006666;
  text-decoration: underline;
}

/* Responsive adjustments */
@media (max-width: 1200px) {
  .off-topic-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .off-topic-grid {
    grid-template-columns: 1fr;
  }
}
</style> 