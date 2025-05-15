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

## 🎬 7 movies for the 7th art

Here are my 7 all-time favorite movies:

1. **Blade Runner** (1982) - A visionary sci-fi masterpiece that redefined the genre
2. **La Strada** (1954) - Fellini's poetic journey of human connection
3. **Anatomy of a Fall** (2023) - A compelling exploration of truth and perspective
4. **Brokeback Mountain** (2005) - A powerful story of love and longing
5. **The Devil, Probably** (1977) - Bresson's profound meditation on modern life
6. **Casablanca** (1942) - The timeless classic of love and sacrifice
7. **The Great Gatsby** (2013) - A visually stunning adaptation of the American dream

## 🎵 Currently Listening

<div id="spotify-player">
  <div class="spotify-container">
    <iframe style="border-radius:12px" 
            src="https://open.spotify.com/embed/track/2fRF1w5mM5ZIUvZvHswpdw?utm_source=generator" 
            width="100%" 
            height="352" 
            frameBorder="0" 
            allowfullscreen="" 
            allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" 
            loading="lazy">
    </iframe>
    <p class="spotify-note"><em>This updates whenever I find a song worth sharing!</em></p>
  </div>
</div>

## 🏃‍♂️ Sports Corner

[Read my sports thoughts and updates](/off-topic/sports/)

## 💧 Water Tracking

<div id="water-tracker">
  <div class="water-stats">
    <h3>Today's Water Intake</h3>
    <div class="water-counter">
      <span id="water-count">0</span> / 2000 ml
    </div>
    <div class="water-progress">
      <div id="water-progress-bar" class="progress-bar"></div>
    </div>
    <div class="water-buttons">
      <button onclick="addWater(250)">+250ml</button>
      <button onclick="addWater(500)">+500ml</button>
      <button onclick="resetWater()" class="reset-button">Reset</button>
    </div>
    <p class="water-note"><em>I track my water intake as a reminder to stay hydrated throughout the day.</em></p>
  </div>
</div>

## 🌟 Duolingo Streak

<div id="duolingo-streak">
  <div class="streak-container">
    <h3>Current Streak</h3>
    <div id="streak-count">Loading...</div>
    <div id="streak-calendar"></div>
  </div>
</div>

<script>
// Water tracking functionality
let waterCount = 0;
const waterGoal = 2000;

function updateProgressBar() {
  const progress = (waterCount / waterGoal) * 100;
  document.getElementById('water-progress-bar').style.width = `${Math.min(progress, 100)}%`;
}

function addWater(amount) {
  waterCount += amount;
  document.getElementById('water-count').textContent = waterCount;
  localStorage.setItem('waterCount', waterCount);
  localStorage.setItem('lastUpdated', new Date().toDateString());
  updateProgressBar();
}

function resetWater() {
  waterCount = 0;
  document.getElementById('water-count').textContent = waterCount;
  localStorage.setItem('waterCount', 0);
  localStorage.setItem('lastUpdated', new Date().toDateString());
  updateProgressBar();
}

// Load saved water count
window.onload = function() {
  const savedCount = localStorage.getItem('waterCount');
  const lastUpdated = localStorage.getItem('lastUpdated');
  
  if (lastUpdated !== new Date().toDateString()) {
    waterCount = 0;
    localStorage.setItem('waterCount', 0);
  } else if (savedCount) {
    waterCount = parseInt(savedCount);
    document.getElementById('water-count').textContent = waterCount;
  }
  updateProgressBar();
}

// Duolingo API integration
async function fetchDuolingoStreak() {
  try {
    const userId = 'jyanqa';
    const response = await fetch(`https://www.duolingo.com/2017-06-30/users/${userId}?fields=streak`);
    const data = await response.json();
    document.getElementById('streak-count').textContent = `${data.streak} days`;
  } catch (error) {
    console.error('Error fetching Duolingo streak:', error);
    document.getElementById('streak-count').textContent = 'Unable to load streak';
  }
}

// Call Duolingo API on page load
fetchDuolingoStreak();
</script>

<style>
.water-stats {
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 8px;
  margin: 20px 0;
}

.water-counter {
  font-size: 24px;
  font-weight: bold;
  color: #008080;
  margin: 15px 0;
}

.water-progress {
  width: 100%;
  height: 10px;
  background-color: #e9ecef;
  border-radius: 5px;
  margin: 15px 0;
  overflow: hidden;
}

.progress-bar {
  height: 100%;
  background-color: #008080;
  width: 0;
  transition: width 0.3s ease;
}

.water-buttons {
  display: flex;
  gap: 10px;
  margin: 15px 0;
}

.water-buttons button {
  background-color: #008080;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.water-buttons button:hover {
  background-color: #006666;
}

.water-buttons .reset-button {
  background-color: #dc3545;
}

.water-buttons .reset-button:hover {
  background-color: #c82333;
}

.water-note {
  font-style: italic;
  color: #666;
  margin-top: 10px;
}

.streak-container {
  background-color: #f8f9fa;
  padding: 20px;
  border-radius: 8px;
  margin: 20px 0;
}

#streak-count {
  font-size: 24px;
  font-weight: bold;
  color: #008080;
  margin: 15px 0;
}

#spotify-player {
  margin: 20px 0;
}

#duolingo-streak {
  margin: 20px 0;
}
</style> 