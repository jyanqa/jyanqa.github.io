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

## 🎬 Movies

1. Blade Runner (1982)
2. La Strada (1954)
3. Anatomy of a Fall (2023)
4. Brokeback Mountain (2005)
5. The Devil, Probably (1977)
6. Casablanca (1942)
7. The Great Gatsby (2013)

## 🎵 Music

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

## 🏃‍♂️ Sports

[Read my sports thoughts and updates](/off-topic/sports/)

## 💧 Water Intake

<div id="water-tracker">
  <div class="water-stats">
    <h3>Daily Water Intake</h3>
    <div class="water-graph">
      <canvas id="waterChart"></canvas>
    </div>
    <div class="water-summary">
      <p>Last month average: 1.5L/day</p>
      <p>Last 3 months average: 1.2L/day</p>
    </div>
  </div>
</div>

## 🌟 Language Learning

<div class="duolingo-section">
  <p>Learning French on Duolingo! <a href="https://www.duolingo.com/profile/jyanqa" target="_blank">Follow my progress</a></p>
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
      data: Array.from({length: 30}, () => 1.2 + Math.random() * 0.6), // Simulated data
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
.water-stats {
  background-color: #f8f9fa;
  padding: 15px;
  border-radius: 8px;
  margin: 15px 0;
}

.water-graph {
  height: 200px;
  margin: 10px 0;
}

.water-summary {
  font-size: 0.9em;
  color: #666;
  margin-top: 10px;
}

.spotify-mini {
  max-width: 300px;
  margin: 10px 0;
}

.duolingo-section {
  background-color: #f8f9fa;
  padding: 10px;
  border-radius: 8px;
  margin: 10px 0;
  font-size: 0.9em;
}

.duolingo-section a {
  color: #008080;
  text-decoration: underline;
}

.duolingo-section a:hover {
  color: #006666;
}
</style> 