---
title: "off topic"
permalink: /off-topic/
layout: single
author_profile: true
---

<div class="off-topic-container">
  <p class="page-description">Trying to add a bit more of human touch in this AI oriented content website</p>

  <div class="page-content">
    <div class="main-content">
      <h2>Sports</h2>
      <div class="sports-section">
        <a href="/off-topic/sports/?v=1" class="sports-btn">Sports Updates</a>
      </div>

      <h2>Language Learning</h2>
      <div class="language-section">
        <p>I am fluent in Vietnamese, English, and Italian. Currently learning French for fun! <a href="https://www.duolingo.com/profile/jyanqa?v=1" target="_blank">via Duolingo</a></p>
      </div>

      <h2>Movies</h2>
      <div class="movies-section">
        <p class="movie-note">These are my favorite movies:</p>
        <div class="movie-list">
          <div class="movie-item">Blade Runner (1982)</div>
          <div class="movie-item">La Strada (1954)</div>
          <div class="movie-item">Anatomy of a Fall (2023)</div>
          <div class="movie-item">Brokeback Mountain (2005)</div>
          <div class="movie-item">The Devil, Probably (1977)</div>
          <div class="movie-item">Casablanca (1942)</div>
          <div class="movie-item">The Great Gatsby (2013)</div>
        </div>
        <div class="movie-actions">
          <a href="/off-topic/movies/?v=1" class="movie-thoughts-btn">Share Movie Thoughts</a>
        </div>
      </div>
    </div>

    <div class="sidebar">
      <h2>Music</h2>
      <div class="music-section">
        <div class="music-player">
          <iframe 
            width="100%" 
            height="60" 
            src="https://www.youtube.com/embed/vMftCgwnR_c?autoplay=0" 
            title="YouTube music player" 
            frameborder="0" 
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen>
          </iframe>
        </div>
        <p class="music-note">my recent obsession I keep in loop: <a href="https://www.youtube.com/watch?v=vMftCgwnR_c" target="_blank">I Will Survive</a></p>
      </div>
    </div>
  </div>
</div>

<style>
.off-topic-container {
  margin-top: 0;
  padding-top: 0;
}

.page-description {
  font-size: 1.1em;
  color: #666;
  margin: 0 0 30px 0;
  font-style: italic;
}

.page-content {
  display: flex;
  gap: 40px;
  margin: 0;
  align-items: flex-start;
}

.main-content {
  flex: 1;
  min-width: 0;
}

.sidebar {
  width: 45%;
  min-width: 0;
  position: sticky;
  top: 2em;
}

.music-section {
  margin: 15px 0;
}

.music-player {
  max-width: 300px;
  margin: 10px 0;
  border-radius: 4px;
  overflow: hidden;
}

.music-note {
  font-size: 0.9em;
  color: #666;
  margin-top: 5px;
}

.language-section {
  background-color: #f8f9fa;
  padding: 15px;
  border-radius: 8px;
  margin: 10px 0;
  font-size: 0.9em;
}

.movies-section {
  margin: 15px 0;
}

.movie-note {
  font-size: 0.9em;
  color: #666;
  margin-bottom: 10px;
}

.movie-list {
  margin-bottom: 15px;
  font-size: 0.9em;
}

.movie-item {
  margin: 5px 0;
  padding-left: 20px;
  position: relative;
}

.movie-item:before {
  content: "•";
  position: absolute;
  left: 0;
  color: #008080;
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

a {
  color: #008080;
  text-decoration: none;
}

a:hover {
  color: #006666;
  text-decoration: underline;
}

.sports-section {
  margin: 10px 0;
}

.sports-btn {
  display: inline-block;
  background-color: #008080;
  color: white;
  padding: 6px 12px;
  border-radius: 4px;
  text-decoration: none;
  font-size: 0.85em;
  transition: background-color 0.3s;
}

.sports-btn:hover {
  background-color: #006666;
  color: white;
  text-decoration: none;
}

@media (max-width: 768px) {
  .page-content {
    flex-direction: column;
    gap: 20px;
  }
  
  .sidebar {
    width: 100%;
    position: static;
  }
}
</style> 