# The_algorithm
THE ALGORITHM KNOWS YOU TOO WELL PROBLEM STATEMENT Students spend significant time scrolling short-form content. Much of it may be harmless entertainment but provide little educational or career value.  Build an AI-powered recommendation agent that analyzes the Reels a student interacts with, infers their underlying interests, and recommends engagi
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The Algorithm Knows You Too Well | AI Recommendation Engine</title>
  <meta name="description" content="AI-Powered Recommendation Agent that analyzes student Reel interactions, infers underlying technical interests beyond keyword matching, and recommends engaging educational tech content.">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;600;700&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
/* ==========================================================================
   THE ALGORITHM KNOWS YOU TOO WELL - DESIGN SYSTEM
   Modern, Precision-Crafted Technical UI
   ========================================================================== */

:root {
  --bg-main: #090d16;
  --bg-card: #111827;
  --bg-card-hover: #162032;
  --bg-card-elevated: #1e293b;
  --bg-input: #0f172a;
  
  --border-subtle: #1e293b;
  --border-medium: #334155;
  --border-active: #38bdf8;

  --text-primary: #f8fafc;
  --text-secondary: #94a3b8;
  --text-muted: #64748b;
  --text-highlight: #38bdf8;

  --color-cyan: #38bdf8;
  --color-emerald: #10b981;
  --color-amber: #f59e0b;
  --color-rose: #f43f5e;
  --color-blue: #3b82f6;

  --font-sans: 'Plus Jakarta Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --font-mono: 'JetBrains Mono', 'Fira Code', Consolas, monospace;

  --radius-sm: 6px;
  --radius-md: 10px;
  --radius-lg: 16px;
  --radius-full: 9999px;

  --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.4);
  --shadow-md: 0 4px 12px -2px rgba(0, 0, 0, 0.5);
  --shadow-lg: 0 12px 28px -4px rgba(0, 0, 0, 0.6);
  --transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: var(--font-sans);
  background-color: var(--bg-main);
  color: var(--text-primary);
  min-height: 100vh;
  line-height: 1.5;
  -webkit-font-smoothing: antialiased;
  overflow-x: hidden;
}

/* ==========================================================================
   Header & Navigation
   ========================================================================== */

.app-header {
  background-color: rgba(17, 24, 39, 0.85);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border-subtle);
  position: sticky;
  top: 0;
  z-index: 100;
  padding: 12px 24px;
}

.header-container {
  max-width: 1440px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 16px;
}

.brand-group {
  display: flex;
  align-items: center;
  gap: 14px;
}

.brand-badge {
  background: linear-gradient(135deg, #0284c7, #0369a1);
  color: #fff;
  font-size: 0.72rem;
  font-weight: 800;
  letter-spacing: 0.08em;
  padding: 4px 8px;
  border-radius: var(--radius-sm);
  box-shadow: 0 2px 4px rgba(0,0,0,0.3);
}

.brand-title {
  font-size: 1.15rem;
  font-weight: 800;
  letter-spacing: -0.02em;
  color: var(--text-primary);
}

.brand-subtitle {
  font-size: 0.78rem;
  color: var(--text-secondary);
  font-weight: 500;
}

.header-actions {
  display: flex;
  align-items: center;
  gap: 12px;
}

.nav-tabs {
  display: flex;
  background-color: var(--bg-input);
  padding: 4px;
  border-radius: var(--radius-md);
  border: 1px solid var(--border-subtle);
  gap: 4px;
}

.tab-btn {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 8px 16px;
  border: none;
  background: transparent;
  color: var(--text-secondary);
  font-family: var(--font-sans);
  font-size: 0.82rem;
  font-weight: 600;
  border-radius: var(--radius-sm);
  cursor: pointer;
  transition: var(--transition);
}

.tab-btn:hover {
  color: var(--text-primary);
  background-color: rgba(255, 255, 255, 0.04);
}

.tab-btn.active {
  background-color: var(--bg-card-elevated);
  color: var(--color-cyan);
  box-shadow: var(--shadow-sm);
}

.tab-icon {
  width: 16px;
  height: 16px;
}

.btn-icon-toggle {
  position: relative;
  background-color: var(--bg-input);
  border: 1px solid var(--border-subtle);
  color: var(--text-primary);
  width: 38px;
  height: 38px;
  border-radius: var(--radius-md);
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: var(--transition);
}

.btn-icon-toggle:hover {
  border-color: var(--color-cyan);
  color: var(--color-cyan);
}

.badge-count {
  position: absolute;
  top: -4px;
  right: -4px;
  background-color: var(--color-cyan);
  color: #030712;
  font-size: 0.65rem;
  font-weight: 800;
  width: 18px;
  height: 18px;
  border-radius: var(--radius-full);
  display: flex;
  align-items: center;
  justify-content: center;
}

/* ==========================================================================
   Main Layout & Panels
   ========================================================================== */

.main-layout {
  max-width: 1440px;
  margin: 0 auto;
  padding: 24px;
}

.tab-pane {
  display: none;
}

.tab-pane.active {
  display: block;
}

.panel {
  background-color: var(--bg-card);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-lg);
  padding: 20px;
  box-shadow: var(--shadow-md);
}

.panel-header {
  margin-bottom: 16px;
}

.panel-header h2 {
  font-size: 1.15rem;
  font-weight: 700;
  letter-spacing: -0.01em;
  color: var(--text-primary);
  margin-top: 4px;
}

.panel-tag {
  display: inline-block;
  font-size: 0.68rem;
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--text-secondary);
  background-color: var(--bg-card-elevated);
  padding: 2px 8px;
  border-radius: var(--radius-sm);
}

.tag-primary {
  color: var(--color-cyan);
  background-color: rgba(56, 189, 248, 0.1);
  border: 1px solid rgba(56, 189, 248, 0.2);
}

.tag-success {
  color: var(--color-emerald);
  background-color: rgba(16, 185, 129, 0.1);
  border: 1px solid rgba(16, 185, 129, 0.2);
}

.phone-top-controls {
  display: flex;
  gap: 8px;
}

/* ==========================================================================
   Feed Simulator Grid (3 Columns)
   ========================================================================== */

.feed-grid {
  display: grid;
  grid-template-columns: 380px 1fr 340px;
  gap: 20px;
  align-items: start;
}

@media (max-width: 1200px) {
  .feed-grid {
    grid-template-columns: 360px 1fr;
  }
  .right-column {
    grid-column: span 2;
  }
}

@media (max-width: 860px) {
  .feed-grid {
    grid-template-columns: 1fr;
  }
  .right-column {
    grid-column: span 1;
  }
}

/* ==========================================================================
   Phone Mockup Simulator
   ========================================================================== */

.phone-frame {
  background-color: #030712;
  border: 3px solid #1f2937;
  border-radius: 36px;
  padding: 12px;
  position: relative;
  box-shadow: 0 20px 40px -10px rgba(0, 0, 0, 0.8);
}

.phone-speaker {
  width: 50px;
  height: 4px;
  background-color: #374151;
  border-radius: 2px;
  margin: 4px auto 10px;
}

.phone-screen {
  background-color: #0b0f19;
  border-radius: 24px;
  overflow: hidden;
  position: relative;
  height: 490px;
  border: 1px solid #1f2937;
}

.reel-media-viewport {
  width: 100%;
  height: 100%;
  position: relative;
  background-color: #020617;
}

#media-canvas {
  width: 100%;
  height: 100%;
  display: block;
}

.media-overlay-badge {
  position: absolute;
  top: 14px;
  left: 14px;
  background: rgba(15, 23, 42, 0.85);
  backdrop-filter: blur(8px);
  color: var(--color-cyan);
  font-size: 0.72rem;
  font-weight: 700;
  padding: 4px 10px;
  border-radius: var(--radius-full);
  border: 1px solid rgba(56, 189, 248, 0.3);
}

.play-indicator-pill {
  position: absolute;
  top: 14px;
  right: 14px;
  background: rgba(16, 185, 129, 0.85);
  color: #fff;
  font-size: 0.65rem;
  font-weight: 800;
  padding: 3px 8px;
  border-radius: var(--radius-full);
}

.screen-nav-btn {
  position: absolute;
  right: 14px;
  width: 28px;
  height: 28px;
  background: rgba(15, 23, 42, 0.7);
  border: 1px solid rgba(255, 255, 255, 0.15);
  color: #fff;
  border-radius: var(--radius-full);
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.7rem;
  transition: var(--transition);
  z-index: 10;
}

.prev-btn { top: 60px; }
.next-btn { top: 96px; }

.screen-nav-btn:hover {
  background: rgba(56, 189, 248, 0.4);
  transform: scale(1.1);
}

.reel-info-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 54px;
  padding: 16px 14px;
  background: linear-gradient(to top, rgba(3, 7, 18, 0.95) 0%, rgba(3, 7, 18, 0.7) 70%, transparent 100%);
  pointer-events: none;
}

.reel-creator-row {
  display: flex;
  align-items: center;
  gap: 8px;
  margin-bottom: 6px;
  pointer-events: auto;
}

.avatar-circle {
  width: 28px;
  height: 28px;
  border-radius: var(--radius-full);
  background-color: #0284c7;
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.75rem;
  font-weight: 700;
}

.creator-handle {
  font-size: 0.82rem;
  font-weight: 700;
  color: #fff;
}

.creator-follow-btn {
  font-size: 0.7rem;
  font-weight: 700;
  color: var(--color-cyan);
  background: transparent;
  border: 1px solid rgba(56, 189, 248, 0.4);
  padding: 1px 8px;
  border-radius: var(--radius-sm);
  margin-left: 4px;
  cursor: pointer;
  transition: var(--transition);
}

.creator-follow-btn:hover {
  background: rgba(56, 189, 248, 0.2);
}

.creator-follow-btn.following {
  background: rgba(16, 185, 129, 0.2);
  color: var(--color-emerald);
  border-color: var(--color-emerald);
}

.reel-caption {
  font-size: 0.8rem;
  color: #f1f5f9;
  line-height: 1.35;
  margin-bottom: 6px;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.reel-tags-row {
  display: flex;
  flex-wrap: wrap;
  gap: 4px;
  margin-bottom: 6px;
}

.reel-pill {
  font-size: 0.68rem;
  color: var(--color-cyan);
  font-weight: 600;
}

.audio-ticker {
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: 0.7rem;
  color: var(--text-secondary);
}

/* Floating Actions on Phone */
.reel-actions-rail {
  position: absolute;
  right: 8px;
  bottom: 24px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  align-items: center;
}

.action-circle-btn {
  background: rgba(30, 41, 59, 0.7);
  backdrop-filter: blur(8px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  width: 38px;
  height: 38px;
  border-radius: var(--radius-full);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: #fff;
  cursor: pointer;
  transition: var(--transition);
}

.action-circle-btn:hover {
  background: rgba(56, 189, 248, 0.3);
  transform: scale(1.08);
}

.action-circle-btn.liked {
  color: var(--color-rose);
}

.action-circle-btn.saved {
  color: var(--color-amber);
}

.action-icon {
  width: 17px;
  height: 17px;
}

.action-count {
  font-size: 0.6rem;
  font-weight: 700;
  margin-top: 1px;
}

/* Phone Controls */
.phone-controls {
  margin-top: 14px;
  padding: 6px;
}

.control-row {
  display: flex;
  justify-content: space-between;
  font-size: 0.78rem;
  color: var(--text-secondary);
  margin-bottom: 4px;
}

.slider-val {
  color: var(--color-cyan);
  font-weight: 700;
  font-family: var(--font-mono);
}

.slider-input {
  width: 100%;
  accent-color: var(--color-cyan);
  cursor: pointer;
  margin-bottom: 12px;
}

.preset-reels-selector label {
  font-size: 0.75rem;
  font-weight: 700;
  color: var(--text-secondary);
  display: block;
}

.category-indicator {
  font-size: 0.7rem;
  font-weight: 700;
  color: var(--color-cyan);
}

.reel-thumbnails-bar {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 6px;
}

.thumb-item {
  background-color: var(--bg-card-elevated);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-sm);
  padding: 6px 4px;
  text-align: center;
  cursor: pointer;
  transition: var(--transition);
}

.thumb-item:hover {
  background-color: var(--bg-card-hover);
  border-color: var(--border-medium);
}

.thumb-item.active {
  border-color: var(--color-cyan);
  background-color: rgba(56, 189, 248, 0.12);
}

.thumb-num {
  font-size: 0.65rem;
  font-weight: 800;
  color: var(--text-muted);
}

.thumb-item.active .thumb-num {
  color: var(--color-cyan);
}

.thumb-label {
  font-size: 0.68rem;
  font-weight: 600;
  color: var(--text-primary);
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

/* ==========================================================================
   Center Column & SPEC OUTPUT CARD (Problem Statement Compliance)
   ========================================================================== */

.flex-between {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.copy-actions {
  display: flex;
  gap: 6px;
}

.spec-output-card {
  background-color: #0b0f19;
  border: 1px solid #1e293b;
  border-left: 4px solid var(--color-cyan);
  border-radius: var(--radius-md);
  padding: 18px;
  font-family: var(--font-mono);
  box-shadow: inset 0 0 20px rgba(0,0,0,0.4);
  margin-bottom: 20px;
}

.spec-card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 14px;
  padding-bottom: 8px;
  border-bottom: 1px solid #1e293b;
}

.spec-badge {
  font-size: 0.72rem;
  font-weight: 800;
  color: var(--color-cyan);
  letter-spacing: 0.05em;
}

.spec-status-pill {
  font-size: 0.68rem;
  font-weight: 700;
  background-color: rgba(16, 185, 129, 0.15);
  color: var(--color-emerald);
  border: 1px solid rgba(16, 185, 129, 0.3);
  padding: 2px 8px;
  border-radius: var(--radius-full);
}

.spec-field-group {
  margin-bottom: 12px;
}

.spec-label {
  font-size: 0.72rem;
  font-weight: 700;
  color: #64748b;
  letter-spacing: 0.04em;
  margin-bottom: 2px;
}

.spec-value {
  font-size: 0.88rem;
  line-height: 1.45;
  color: #e2e8f0;
}

.highlight-cyan {
  color: #38bdf8;
  font-weight: 600;
}

.highlight-amber {
  color: #fbbf24;
  font-weight: 600;
}

.highlight-emerald {
  color: #34d399;
  font-weight: 600;
}

.text-subtle {
  color: #94a3b8;
  font-family: var(--font-sans);
  font-size: 0.84rem;
}

.spec-divider {
  height: 1px;
  background: #1e293b;
  margin: 14px 0;
}

.spec-meta-row {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
  margin: 12px 0;
}

.meta-item {
  display: flex;
  align-items: center;
  gap: 6px;
}

.meta-pill {
  font-size: 0.72rem;
  font-weight: 700;
  padding: 2px 8px;
  border-radius: var(--radius-sm);
  background-color: #1e293b;
  color: #f1f5f9;
}

.category-pill {
  background-color: rgba(56, 189, 248, 0.15);
  color: var(--color-cyan);
  border: 1px solid rgba(56, 189, 248, 0.3);
}

.diff-pill {
  background-color: rgba(245, 158, 11, 0.15);
  color: var(--color-amber);
  border: 1px solid rgba(245, 158, 11, 0.3);
}

.conf-pill {
  background-color: rgba(16, 185, 129, 0.15);
  color: var(--color-emerald);
  border: 1px solid rgba(16, 185, 129, 0.3);
}

.rec-action-bar {
  margin-top: 14px;
  padding-top: 10px;
  border-top: 1px solid #1e293b;
}

.btn-preview-rec {
  width: 100%;
  background: rgba(16, 185, 129, 0.15);
  color: var(--color-emerald);
  border: 1px solid rgba(16, 185, 129, 0.3);
  padding: 8px 14px;
  border-radius: var(--radius-sm);
  font-family: var(--font-sans);
  font-size: 0.82rem;
  font-weight: 700;
  cursor: pointer;
  transition: var(--transition);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
}

.btn-preview-rec:hover {
  background: rgba(16, 185, 129, 0.25);
  border-color: var(--color-emerald);
}

/* ==========================================================================
   Reasoning Pipeline Steps
   ========================================================================== */

.reasoning-pipeline {
  background-color: var(--bg-input);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 16px;
}

.section-title {
  font-size: 0.88rem;
  font-weight: 700;
  color: var(--text-primary);
  margin-bottom: 12px;
}

.pipeline-steps {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.step-card {
  display: flex;
  gap: 12px;
  background-color: var(--bg-card);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-sm);
  padding: 10px 12px;
  align-items: flex-start;
}

.step-num {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  font-weight: 800;
  color: var(--color-cyan);
  background: rgba(56, 189, 248, 0.1);
  padding: 2px 6px;
  border-radius: var(--radius-sm);
}

.step-body h4 {
  font-size: 0.8rem;
  font-weight: 700;
  color: var(--text-primary);
}

.step-body p {
  font-size: 0.76rem;
  color: var(--text-secondary);
  margin-top: 2px;
}

.substance-score-tag {
  font-size: 0.7rem;
  font-weight: 700;
  color: var(--color-emerald);
}

/* ==========================================================================
   Right Column: Profile & Vector Radar
   ========================================================================== */

.profile-card {
  background-color: var(--bg-input);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 16px;
  margin-bottom: 16px;
}

.profile-header {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 14px;
  padding-bottom: 10px;
  border-bottom: 1px solid var(--border-subtle);
}

.student-avatar {
  width: 36px;
  height: 36px;
  border-radius: var(--radius-full);
  background: linear-gradient(135deg, #10b981, #047857);
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 800;
  font-size: 0.85rem;
}

.student-info h4 {
  font-size: 0.85rem;
  font-weight: 700;
}

.student-info p {
  font-size: 0.74rem;
  color: var(--text-secondary);
}

.text-emerald {
  color: var(--color-emerald);
}

.vector-breakdown {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.vector-row {
  display: grid;
  grid-template-columns: 130px 1fr 34px;
  align-items: center;
  gap: 8px;
}

.vector-name {
  font-size: 0.74rem;
  color: var(--text-secondary);
  font-weight: 600;
}

.progress-track {
  height: 6px;
  background-color: var(--bg-card-elevated);
  border-radius: var(--radius-full);
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  border-radius: var(--radius-full);
  transition: width 0.4s ease;
}

.fill-java { background-color: #f59e0b; }
.fill-hld { background-color: #38bdf8; }
.fill-dsa { background-color: #10b981; }
.fill-hw { background-color: #a855f7; }
.fill-sec { background-color: #f43f5e; }
.fill-ai { background-color: #06b6d4; }

.vector-pct {
  font-size: 0.72rem;
  font-family: var(--font-mono);
  color: var(--text-muted);
  text-align: right;
}

.conversion-widget {
  background: linear-gradient(135deg, rgba(16, 185, 129, 0.08), rgba(56, 189, 248, 0.05));
  border: 1px solid rgba(16, 185, 129, 0.2);
  border-radius: var(--radius-md);
  padding: 14px;
  display: flex;
  align-items: center;
  gap: 14px;
  margin-bottom: 16px;
}

.metric-circle {
  width: 58px;
  height: 58px;
  border-radius: var(--radius-full);
  background-color: rgba(16, 185, 129, 0.15);
  border: 2px solid var(--color-emerald);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.metric-val {
  font-size: 0.95rem;
  font-weight: 800;
  color: var(--color-emerald);
  line-height: 1;
}

.metric-lbl {
  font-size: 0.52rem;
  text-transform: uppercase;
  color: var(--text-secondary);
  font-weight: 700;
}

.metric-info h4 {
  font-size: 0.8rem;
  font-weight: 700;
  color: var(--text-primary);
}

.metric-info p {
  font-size: 0.72rem;
  color: var(--text-secondary);
  margin-top: 2px;
}

.trap-shortcut-box {
  background-color: var(--bg-card-elevated);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 14px;
}

.trap-shortcut-box h4 {
  font-size: 0.82rem;
  font-weight: 700;
  color: var(--color-cyan);
}

.trap-shortcut-box p {
  font-size: 0.74rem;
  color: var(--text-secondary);
  margin: 4px 0 10px;
}

/* ==========================================================================
   TAB 2: BUILT-IN TRAP ARENA
   ========================================================================== */

.trap-arena-container {
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.arena-header {
  background-color: var(--bg-card);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-lg);
  padding: 24px;
}

.arena-badge {
  display: inline-block;
  font-size: 0.7rem;
  font-weight: 800;
  letter-spacing: 0.08em;
  color: #f59e0b;
  background-color: rgba(245, 158, 11, 0.1);
  border: 1px solid rgba(245, 158, 11, 0.3);
  padding: 3px 10px;
  border-radius: var(--radius-sm);
  margin-bottom: 8px;
}

.arena-header h2 {
  font-size: 1.4rem;
  font-weight: 800;
  letter-spacing: -0.02em;
  margin-bottom: 8px;
}

.arena-desc {
  font-size: 0.88rem;
  color: var(--text-secondary);
  line-height: 1.6;
}

.trap-sequence-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 14px;
}

@media (max-width: 900px) {
  .trap-sequence-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

.sequence-card {
  background-color: var(--bg-card);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 14px;
}

.seq-num {
  font-size: 0.68rem;
  font-weight: 800;
  color: var(--color-cyan);
  margin-bottom: 4px;
}

.seq-title {
  font-size: 0.82rem;
  font-weight: 700;
  color: var(--text-primary);
  margin-bottom: 6px;
}

.seq-cat {
  font-size: 0.68rem;
  color: var(--text-muted);
}

.comparison-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}

@media (max-width: 900px) {
  .comparison-grid {
    grid-template-columns: 1fr;
  }
}

.comp-col {
  background-color: var(--bg-card);
  border-radius: var(--radius-lg);
  padding: 20px;
  border: 1px solid var(--border-subtle);
}

.comp-shallow {
  border-left: 4px solid var(--color-rose);
}

.comp-agent {
  border-left: 4px solid var(--color-emerald);
}

.comp-badge {
  display: inline-block;
  font-size: 0.68rem;
  font-weight: 800;
  letter-spacing: 0.06em;
  padding: 3px 8px;
  border-radius: var(--radius-sm);
  margin-bottom: 6px;
}

.badge-danger {
  color: var(--color-rose);
  background-color: rgba(244, 63, 94, 0.1);
  border: 1px solid rgba(244, 63, 94, 0.3);
}

.badge-success {
  color: var(--color-emerald);
  background-color: rgba(16, 185, 129, 0.1);
  border: 1px solid rgba(16, 185, 129, 0.3);
}

.comp-header h3 {
  font-size: 1.05rem;
  font-weight: 700;
  margin-bottom: 16px;
}

.comp-defect-card {
  background-color: var(--bg-input);
  border: 1px solid rgba(244, 63, 94, 0.2);
  border-radius: var(--radius-md);
  padding: 14px;
  margin-bottom: 12px;
}

.defect-title {
  font-size: 0.78rem;
  font-weight: 700;
  color: var(--color-rose);
  margin-bottom: 4px;
}

.defect-reel {
  font-family: var(--font-mono);
  font-size: 0.82rem;
  color: #f1f5f9;
  font-weight: 600;
  margin-bottom: 6px;
}

.defect-reason {
  font-size: 0.76rem;
  color: var(--text-secondary);
}

.comp-verdict {
  font-size: 0.78rem;
  font-weight: 800;
  padding: 10px;
  border-radius: var(--radius-sm);
  text-align: center;
  margin-top: 14px;
}

.verdict-danger {
  background-color: rgba(244, 63, 94, 0.15);
  color: var(--color-rose);
  border: 1px solid rgba(244, 63, 94, 0.3);
}

.verdict-success {
  background-color: rgba(16, 185, 129, 0.15);
  color: var(--color-emerald);
  border: 1px solid rgba(16, 185, 129, 0.3);
}

.trap-agent-card {
  margin-bottom: 0;
}

/* ==========================================================================
   TAB 3: CUSTOM SANDBOX
   ========================================================================== */

.sandbox-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}

@media (max-width: 900px) {
  .sandbox-container {
    grid-template-columns: 1fr;
  }
}

.presets-row {
  display: flex;
  align-items: center;
  gap: 8px;
  margin-bottom: 14px;
  flex-wrap: wrap;
}

.preset-label {
  font-size: 0.75rem;
  font-weight: 700;
  color: var(--text-secondary);
}

.sandbox-form {
  display: flex;
  flex-direction: column;
  gap: 14px;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.form-group label {
  font-size: 0.78rem;
  font-weight: 700;
  color: var(--text-secondary);
}

.form-input, .form-textarea, .form-select {
  background-color: var(--bg-input);
  border: 1px solid var(--border-medium);
  border-radius: var(--radius-sm);
  padding: 10px 12px;
  color: var(--text-primary);
  font-family: var(--font-sans);
  font-size: 0.85rem;
  transition: var(--transition);
}

.form-input:focus, .form-textarea:focus, .form-select:focus {
  outline: none;
  border-color: var(--color-cyan);
  box-shadow: 0 0 0 2px rgba(56, 189, 248, 0.2);
}

.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
}

.flex-align-end {
  justify-content: flex-end;
}

.checkbox-row {
  display: flex;
  gap: 16px;
  font-size: 0.8rem;
  font-weight: 600;
  padding-bottom: 8px;
}

.checkbox-row label {
  display: flex;
  align-items: center;
  gap: 6px;
  cursor: pointer;
}

.form-actions {
  display: flex;
  gap: 10px;
  margin-top: 4px;
}

.badge-filter-status {
  font-size: 0.68rem;
  font-weight: 800;
  padding: 2px 8px;
  border-radius: var(--radius-sm);
  background-color: rgba(56, 189, 248, 0.15);
  color: var(--color-cyan);
  border: 1px solid rgba(56, 189, 248, 0.3);
}

.placeholder-text {
  font-size: 0.85rem;
  color: var(--text-muted);
  text-align: center;
  padding: 40px 20px;
}

/* ==========================================================================
   TAB 4: TECH REEL CATALOG
   ========================================================================== */

.catalog-filters {
  display: flex;
  gap: 6px;
  flex-wrap: wrap;
}

.cat-filter-btn {
  background-color: var(--bg-card-elevated);
  border: 1px solid var(--border-subtle);
  color: var(--text-secondary);
  padding: 4px 10px;
  border-radius: var(--radius-sm);
  font-size: 0.72rem;
  font-weight: 700;
  cursor: pointer;
  transition: var(--transition);
}

.cat-filter-btn:hover {
  color: var(--text-primary);
  border-color: var(--border-medium);
}

.cat-filter-btn.active {
  background-color: rgba(56, 189, 248, 0.15);
  color: var(--color-cyan);
  border-color: rgba(56, 189, 248, 0.3);
}

.catalog-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 16px;
  margin-top: 16px;
}

.catalog-card {
  background-color: var(--bg-input);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 16px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: var(--transition);
}

.catalog-card:hover {
  border-color: var(--border-medium);
  transform: translateY(-2px);
}

.cat-card-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 8px;
}

.cat-card-title {
  font-size: 0.88rem;
  font-weight: 700;
  color: var(--text-primary);
  line-height: 1.35;
  margin-bottom: 6px;
}

.cat-card-desc {
  font-size: 0.78rem;
  color: var(--text-secondary);
  margin-bottom: 12px;
  line-height: 1.45;
}

.cat-takeaways {
  list-style: none;
  margin-bottom: 12px;
}

.cat-takeaways li {
  font-size: 0.74rem;
  color: var(--color-cyan);
  margin-bottom: 4px;
}

.cat-takeaways li::before {
  content: "✓ ";
  color: var(--color-emerald);
}

.cat-card-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 10px;
  border-top: 1px solid var(--border-subtle);
}

/* ==========================================================================
   TAB 5: FULL REPORT
   ========================================================================== */

.report-content {
  background-color: #0b0f19;
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 20px;
  font-family: var(--font-mono);
  font-size: 0.82rem;
  line-height: 1.6;
  white-space: pre-wrap;
  color: #e2e8f0;
  max-height: 650px;
  overflow-y: auto;
}

/* ==========================================================================
   Modals & Drawers
   ========================================================================== */

.modal-backdrop, .drawer-backdrop {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: rgba(3, 7, 18, 0.75);
  backdrop-filter: blur(8px);
  z-index: 200;
  display: none;
  align-items: center;
  justify-content: center;
  padding: 20px;
}

.modal-backdrop.active, .drawer-backdrop.active {
  display: flex;
}

.modal-window {
  background-color: var(--bg-card);
  border: 1px solid var(--border-medium);
  border-radius: var(--radius-lg);
  width: 100%;
  max-width: 580px;
  box-shadow: var(--shadow-lg);
  overflow: hidden;
  animation: modalPop 0.2s cubic-bezier(0.16, 1, 0.3, 1);
}

@keyframes modalPop {
  from { opacity: 0; transform: scale(0.95); }
  to { opacity: 1; transform: scale(1); }
}

.modal-header {
  padding: 16px 20px;
  border-bottom: 1px solid var(--border-subtle);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.modal-badge {
  font-size: 0.7rem;
  font-weight: 800;
  color: var(--color-emerald);
  letter-spacing: 0.06em;
}

.modal-close-btn {
  background: transparent;
  border: none;
  color: var(--text-secondary);
  font-size: 1.1rem;
  cursor: pointer;
  transition: var(--transition);
}

.modal-close-btn:hover {
  color: var(--text-primary);
}

.modal-body {
  padding: 20px;
  max-height: 70vh;
  overflow-y: auto;
}

.modal-reel-title {
  font-size: 1.05rem;
  font-weight: 700;
  margin-bottom: 4px;
}

.modal-reel-creator {
  font-size: 0.78rem;
  color: var(--text-secondary);
  margin-bottom: 14px;
}

.modal-canvas-wrapper {
  background-color: #030712;
  border-radius: var(--radius-md);
  border: 1px solid var(--border-subtle);
  overflow: hidden;
  margin-bottom: 16px;
  height: 220px;
}

#modal-media-canvas {
  width: 100%;
  height: 100%;
  display: block;
}

.modal-section {
  margin-bottom: 14px;
}

.modal-section h4 {
  font-size: 0.82rem;
  font-weight: 700;
  color: var(--color-cyan);
  margin-bottom: 6px;
}

.takeaways-list {
  padding-left: 18px;
  font-size: 0.8rem;
  color: #e2e8f0;
  line-height: 1.5;
}

.modal-rationale {
  font-size: 0.8rem;
  color: var(--text-secondary);
  line-height: 1.5;
}

.modal-footer {
  padding: 14px 20px;
  border-top: 1px solid var(--border-subtle);
}

/* Slide-over Drawer */
.drawer-backdrop {
  justify-content: flex-end;
  padding: 0;
}

.drawer-panel {
  background-color: var(--bg-card);
  border-left: 1px solid var(--border-medium);
  width: 100%;
  max-width: 420px;
  height: 100%;
  box-shadow: var(--shadow-lg);
  display: flex;
  flex-direction: column;
  animation: drawerSlide 0.25s cubic-bezier(0.16, 1, 0.3, 1);
}

@keyframes drawerSlide {
  from { transform: translateX(100%); }
  to { transform: translateX(0); }
}

.drawer-header {
  padding: 20px;
  border-bottom: 1px solid var(--border-subtle);
}

.drawer-body {
  padding: 20px;
  flex: 1;
  overflow-y: auto;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.drawer-item {
  background-color: var(--bg-input);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-md);
  padding: 12px;
  cursor: pointer;
  transition: var(--transition);
}

.drawer-item:hover {
  border-color: var(--color-cyan);
}

.drawer-item-title {
  font-size: 0.82rem;
  font-weight: 700;
  color: var(--text-primary);
  margin-bottom: 4px;
}

.drawer-item-cat {
  font-size: 0.7rem;
  color: var(--color-cyan);
}

/* Comments Modal */
.comment-item {
  display: flex;
  gap: 10px;
  margin-bottom: 14px;
  padding-bottom: 10px;
  border-bottom: 1px solid var(--border-subtle);
}

.comment-avatar {
  width: 30px;
  height: 30px;
  border-radius: var(--radius-full);
  background-color: #334155;
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.72rem;
  font-weight: 700;
  flex-shrink: 0;
}

.comment-user {
  font-size: 0.76rem;
  font-weight: 700;
  color: #f1f5f9;
}

.comment-time {
  font-size: 0.68rem;
  color: var(--text-muted);
  margin-left: 6px;
}

.comment-text {
  font-size: 0.78rem;
  color: var(--text-secondary);
  margin-top: 2px;
}

/* Share Modal */
.share-box {
  display: flex;
  gap: 8px;
  margin-bottom: 16px;
}

.share-options-row {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.share-pill {
  background-color: var(--bg-input);
  border: 1px solid var(--border-medium);
  color: var(--text-primary);
  padding: 8px 14px;
  border-radius: var(--radius-sm);
  font-size: 0.78rem;
  font-weight: 600;
  cursor: pointer;
  transition: var(--transition);
}

.share-pill:hover {
  border-color: var(--color-cyan);
  color: var(--color-cyan);
}

/* ==========================================================================
   Toast Notification System
   ========================================================================== */

.toast-container {
  position: fixed;
  bottom: 24px;
  right: 24px;
  z-index: 300;
  display: flex;
  flex-direction: column;
  gap: 8px;
  pointer-events: none;
}

.toast-item {
  background-color: #0f172a;
  border: 1px solid var(--color-cyan);
  color: #f8fafc;
  padding: 10px 16px;
  border-radius: var(--radius-md);
  font-size: 0.82rem;
  font-weight: 600;
  box-shadow: var(--shadow-lg);
  display: flex;
  align-items: center;
  gap: 8px;
  animation: toastIn 0.2s cubic-bezier(0.16, 1, 0.3, 1);
  pointer-events: auto;
}

@keyframes toastIn {
  from { opacity: 0; transform: translateY(12px); }
  to { opacity: 1; transform: translateY(0); }
}

/* ==========================================================================
   Buttons & Utilities
   ========================================================================== */

.btn-primary {
  background: linear-gradient(135deg, #0284c7, #0369a1);
  color: #fff;
  border: none;
  border-radius: var(--radius-sm);
  padding: 10px 18px;
  font-family: var(--font-sans);
  font-size: 0.85rem;
  font-weight: 700;
  cursor: pointer;
  transition: var(--transition);
}

.btn-primary:hover {
  background: linear-gradient(135deg, #0369a1, #075985);
  box-shadow: 0 4px 12px rgba(2, 132, 199, 0.3);
}

.btn-sm {
  background-color: var(--bg-card-elevated);
  border: 1px solid var(--border-medium);
  color: var(--text-primary);
  border-radius: var(--radius-sm);
  padding: 6px 12px;
  font-size: 0.76rem;
  font-weight: 600;
  cursor: pointer;
  transition: var(--transition);
  display: inline-flex;
  align-items: center;
  gap: 6px;
}

.btn-sm:hover {
  background-color: var(--bg-card-hover);
  border-color: var(--color-cyan);
  color: var(--color-cyan);
}

.btn-micro {
  background-color: var(--bg-card-elevated);
  border: 1px solid var(--border-subtle);
  color: var(--text-secondary);
  font-size: 0.7rem;
  font-weight: 600;
  padding: 3px 8px;
  border-radius: var(--radius-sm);
  cursor: pointer;
  transition: var(--transition);
}

.btn-micro:hover {
  color: var(--color-cyan);
  border-color: var(--color-cyan);
}

.btn-group {
  display: flex;
  gap: 8px;
}

.w-full {
  width: 100%;
}

.mb-4 { margin-bottom: 4px; }
.mb-12 { margin-bottom: 12px; }

</style>
</head>
<body>
  <!-- Header -->
  <header class="app-header">
    <div class="header-container">
      <div class="brand-group">
        <div class="brand-badge">AI AGENT</div>
        <div class="brand-text">
          <h1 class="brand-title">THE ALGORITHM KNOWS YOU TOO WELL</h1>
          <p class="brand-subtitle">Latent Context Inference • Anti-Hype Filtering • Smart Educational Scaffolding</p>
        </div>
      </div>
      <div class="header-actions">
        <nav class="nav-tabs" role="tablist">
          <button class="tab-btn active" data-tab="tab-feed" id="tab-btn-feed">
            <svg class="tab-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="5" y="2" width="14" height="20" rx="2" ry="2"></rect><line x1="12" y1="18" x2="12.01" y2="18"></line></svg>
            Feed Simulator
          </button>
          <button class="tab-btn" data-tab="tab-trap" id="tab-btn-trap">
            <svg class="tab-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"></path><line x1="12" y1="9" x2="12" y2="13"></line><line x1="12" y1="17" x2="12.01" y2="17"></line></svg>
            Built-In Trap Arena
          </button>
          <button class="tab-btn" data-tab="tab-sandbox" id="tab-btn-sandbox">
            <svg class="tab-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"></polyline><polyline points="8 6 2 12 8 18"></polyline></svg>
            Custom Sandbox
          </button>
          <button class="tab-btn" data-tab="tab-catalog" id="tab-btn-catalog">
            <svg class="tab-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="7" height="7"></rect><rect x="14" y="3" width="7" height="7"></rect><rect x="14" y="14" width="7" height="7"></rect><rect x="3" y="14" width="7" height="7"></rect></svg>
            Tech Reel Catalog
          </button>
          <button class="tab-btn" data-tab="tab-export" id="tab-btn-export">
            <svg class="tab-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path><polyline points="7 10 12 15 17 10"></polyline><line x1="12" y1="15" x2="12" y2="3"></line></svg>
            Report & Export
          </button>
        </nav>
        <button class="btn-icon-toggle" id="btn-saved-drawer" title="View Bookmarked Reels">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M19 21l-7-5-7 5V5a2 2 0 0 1 2-2h10a2 2 0 0 1 2 2z"></path></svg>
          <span class="badge-count" id="saved-badge-count">2</span>
        </button>
      </div>
    </div>
  </header>

  <!-- Main Viewport -->
  <main class="main-layout">
    <!-- TAB 1: FEED SIMULATOR & LIVE INFERENCE -->
    <section id="tab-feed" class="tab-pane active">
      <div class="feed-grid">
        
        <!-- COLUMN 1: Phone Reel Scroll Simulator -->
        <div class="panel phone-column">
          <div class="panel-header flex-between">
            <div>
              <span class="panel-tag">STUDENT INTERFACE</span>
              <h2>Short-Form Reel Simulator</h2>
            </div>
            <div class="phone-top-controls">
              <button class="btn-micro" id="btn-audio-toggle" title="Toggle Procedural Audio Effects">
                <span id="audio-icon">🔊</span> Audio: ON
              </button>
              <button class="btn-micro" id="btn-autoscroll" title="Toggle Auto-Scroll Mode">
                <span id="autoscroll-icon">▶</span> Auto-Scroll
              </button>
            </div>
          </div>
          
          <div class="phone-frame">
            <div class="phone-speaker"></div>
            
            <div class="phone-screen" id="phone-screen">
              <!-- Animated Dynamic Canvas Visualizer -->
              <div class="reel-media-viewport">
                <canvas id="media-canvas" width="340" height="440"></canvas>
                <div class="media-overlay-badge" id="reel-surface-badge">Programming Memes</div>
                <div class="play-indicator-pill" id="play-status">REWATCHING • 1.4x</div>
                
                <!-- Quick Navigation Arrows on Screen -->
                <button class="screen-nav-btn prev-btn" id="btn-prev-reel" title="Previous Reel">▲</button>
                <button class="screen-nav-btn next-btn" id="btn-next-reel" title="Next Reel">▼</button>
              </div>

              <!-- Reel Content Overlay -->
              <div class="reel-info-overlay">
                <div class="reel-creator-row">
                  <div class="avatar-circle" id="reel-avatar">DH</div>
                  <div class="creator-meta">
                    <span class="creator-handle" id="reel-creator">@DevHumorCentral</span>
                    <button class="creator-follow-btn" id="btn-follow">Follow</button>
                  </div>
                </div>
                <p class="reel-caption" id="reel-caption">When you fix 1 bug in Java and 47 NullPointerExceptions spawn in production 💀</p>
                <div class="reel-tags-row" id="reel-tags-container">
                  <span class="reel-pill">#Java</span>
                  <span class="reel-pill">#Memes</span>
                  <span class="reel-pill">#Debugging</span>
                </div>
                <div class="audio-ticker">
                  <span class="audio-note">🎵</span>
                  <span class="audio-title" id="reel-audio">Original Audio • Frantic Bass Crash</span>
                </div>
              </div>

              <!-- Floating Action Rail on Phone -->
              <div class="reel-actions-rail">
                <button class="action-circle-btn" id="btn-like" title="Like Reel">
                  <svg class="action-icon" viewBox="0 0 24 24" fill="currentColor"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>
                  <span class="action-count" id="like-count">142K</span>
                </button>
                <button class="action-circle-btn" id="btn-comments" title="View Simulated Comments">
                  <svg class="action-icon" viewBox="0 0 24 24" fill="currentColor"><path d="M20 2H4c-1.1 0-1.99.9-1.99 2L2 22l4-4h14c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zM6 9h12v2H6V9zm8 5H6v-2h8v2zm4-6H6V6h12v2z"/></svg>
                  <span class="action-count" id="comment-count">1.8K</span>
                </button>
                <button class="action-circle-btn" id="btn-save" title="Save / Bookmark Reel">
                  <svg class="action-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M19 21l-7-5-7 5V5a2 2 0 0 1 2-2h10a2 2 0 0 1 2 2z"></path></svg>
                  <span class="action-count" id="save-count">18.4K</span>
                </button>
                <button class="action-circle-btn" id="btn-share" title="Share Reel & AI Breakdown">
                  <svg class="action-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="18" cy="5" r="3"></circle><circle cx="6" cy="12" r="3"></circle><circle cx="18" cy="19" r="3"></circle><line x1="8.59" y1="13.51" x2="15.42" y2="17.49"></line><line x1="15.41" y1="6.51" x2="8.59" y2="10.49"></line></svg>
                  <span class="action-count">9.2K</span>
                </button>
              </div>
            </div>

            <!-- Controls below phone -->
            <div class="phone-controls">
              <div class="control-row">
                <label for="watch-slider">Engagement Duration / Replay:</label>
                <span class="slider-val" id="watch-val">140% (Re-watched)</span>
              </div>
              <input type="range" id="watch-slider" min="0.2" max="2.5" step="0.1" value="1.4" class="slider-input">
              
              <div class="preset-reels-selector">
                <div class="flex-between mb-4">
                  <label>Select Sample Reel (1 to 8):</label>
                  <span class="category-indicator" id="current-category-indicator">Programming Memes</span>
                </div>
                <div class="reel-thumbnails-bar" id="reels-list">
                  <!-- Injected via JS -->
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- COLUMN 2: Required Recommendation Output Card & Reasoning Pipeline -->
        <div class="panel center-column">
          <div class="panel-header flex-between">
            <div>
              <span class="panel-tag tag-primary">AI RECOMMENDATION ENGINE</span>
              <h2>Real-Time Latent Analysis</h2>
            </div>
            <div class="copy-actions">
              <button class="btn-sm" id="btn-copy-spec" title="Copy Required Text Format">
                <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg>
                Copy Required Spec
              </button>
              <button class="btn-sm" id="btn-copy-json" title="Copy JSON Payload">
                <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"></polyline><polyline points="8 6 2 12 8 18"></polyline></svg>
                Copy JSON
              </button>
            </div>
          </div>

          <!-- THE REQUIRED OUTPUT FORMAT CARD -->
          <div class="spec-output-card" id="spec-card">
            <div class="spec-card-header">
              <div class="spec-badge">REQUIRED OUTPUT FORMAT</div>
              <div class="spec-status-pill" id="spec-confidence-pill">CONFIDENCE: HIGH</div>
            </div>

            <div class="spec-field-group">
              <div class="spec-label">CURRENT REEL:</div>
              <div class="spec-value highlight-cyan" id="out-current-reel">"When you fix 1 bug in Java and 47 NullPointerExceptions spawn in production 💀" (DevHumorCentral)</div>
            </div>

            <div class="spec-field-group">
              <div class="spec-label">INTEREST DETECTED:</div>
              <div class="spec-value highlight-amber" id="out-interest-detected">Java Runtime Mechanics & Enterprise Defensive Programming</div>
            </div>

            <div class="spec-field-group">
              <div class="spec-label">WHY:</div>
              <div class="spec-value text-subtle" id="out-why">Student re-watched a production crash sketch triggered by unhandled NullPointerExceptions at line 132. Rather than merely seeking generic Java syntax, the student is reacting to real backend runtime vulnerabilities, exception handling chaos, and production deployment stress.</div>
            </div>

            <div class="spec-divider"></div>

            <div class="spec-field-group">
              <div class="spec-label">RECOMMENDED TECH REEL:</div>
              <div class="spec-value highlight-emerald" id="out-rec-reel">"Why NullPointerExceptions Happen in Bytecode: Optional vs Null Safety" by ModernJavaEng</div>
            </div>

            <div class="spec-meta-row">
              <div class="meta-item">
                <span class="spec-label">CATEGORY:</span>
                <span class="meta-pill category-pill" id="out-category">Java</span>
              </div>
              <div class="meta-item">
                <span class="spec-label">DIFFICULTY:</span>
                <span class="meta-pill diff-pill" id="out-difficulty">Beginner</span>
              </div>
              <div class="meta-item">
                <span class="spec-label">CONFIDENCE:</span>
                <span class="meta-pill conf-pill" id="out-confidence">High</span>
              </div>
            </div>

            <div class="spec-field-group">
              <div class="spec-label">WHY THIS RECOMMENDATION:</div>
              <div class="spec-value text-subtle" id="out-why-rec">Addresses the exact root cause of the meme by breaking down how the JVM executes bytecode invocations on null references and demonstrating modern Optional/pattern-matching idioms to achieve rock-solid null safety in enterprise Java.</div>
            </div>

            <div class="rec-action-bar">
              <button class="btn-preview-rec" id="btn-preview-rec">
                <span>▶</span> Watch Recommended Tech Reel Preview
              </button>
            </div>
          </div>

          <!-- Multi-Stage AI Reasoning Flow -->
          <div class="reasoning-pipeline">
            <h3 class="section-title">Deep Inference & Anti-Hype Pipeline</h3>
            <div class="pipeline-steps">
              <div class="step-card">
                <div class="step-num">01</div>
                <div class="step-body">
                  <h4>Signal Deconstruction</h4>
                  <p id="step1-desc">Extracted tone: Satirical humor • Interaction: Rewatched (140%) • Intent: Production bug anxiety.</p>
                </div>
              </div>
              <div class="step-card">
                <div class="step-num">02</div>
                <div class="step-body">
                  <h4>Latent Intent Discovery</h4>
                  <p id="step2-desc">Distinguished surface meme from underlying backend runtime & defensive programming curiosity.</p>
                </div>
              </div>
              <div class="step-card">
                <div class="step-num">03</div>
                <div class="step-body">
                  <div class="flex-between">
                    <h4>Anti-Hype & Rigor Screening</h4>
                    <span class="substance-score-tag" id="anti-hype-score">Substance: 95%</span>
                  </div>
                  <p id="step3-desc">Filtered out superficial syntax listicles and hype traps. Elevated architectural bytecode analysis.</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- COLUMN 3: Student Latent Profile & Trajectory -->
        <div class="panel right-column">
          <div class="panel-header flex-between">
            <div>
              <span class="panel-tag tag-success">STUDENT INSIGHTS</span>
              <h2>Latent Interest Graph</h2>
            </div>
            <button class="btn-micro" id="btn-reset-profile" title="Reset Interaction History">Reset</button>
          </div>

          <div class="profile-card">
            <div class="profile-header">
              <div class="student-avatar" id="profile-avatar">ST</div>
              <div class="student-info">
                <h4>Anonymized Student Profile</h4>
                <p>Curiosity State: <strong class="text-emerald" id="student-curiosity-level">High Aptitude</strong></p>
              </div>
            </div>

            <div class="vector-breakdown" id="vector-breakdown-container">
              <div class="vector-row">
                <span class="vector-name">Java & JVM</span>
                <div class="progress-track"><div class="progress-fill fill-java" id="bar-java" style="width: 95%;"></div></div>
                <span class="vector-pct" id="pct-java">95%</span>
              </div>
              <div class="vector-row">
                <span class="vector-name">High-Level Design (HLD)</span>
                <div class="progress-track"><div class="progress-fill fill-hld" id="bar-hld" style="width: 70%;"></div></div>
                <span class="vector-pct" id="pct-hld">70%</span>
              </div>
              <div class="vector-row">
                <span class="vector-name">DSA & Algorithms</span>
                <div class="progress-track"><div class="progress-fill fill-dsa" id="bar-dsa" style="width: 88%;"></div></div>
                <span class="vector-pct" id="pct-dsa">88%</span>
              </div>
              <div class="vector-row">
                <span class="vector-name">Hardware & Systems</span>
                <div class="progress-track"><div class="progress-fill fill-hw" id="bar-hw" style="width: 82%;"></div></div>
                <span class="vector-pct" id="pct-hw">82%</span>
              </div>
              <div class="vector-row">
                <span class="vector-name">Cybersecurity</span>
                <div class="progress-track"><div class="progress-fill fill-sec" id="bar-sec" style="width: 60%;"></div></div>
                <span class="vector-pct" id="pct-sec">60%</span>
              </div>
              <div class="vector-row">
                <span class="vector-name">AI & Transformers</span>
                <div class="progress-track"><div class="progress-fill fill-ai" id="bar-ai" style="width: 65%;"></div></div>
                <span class="vector-pct" id="pct-ai">65%</span>
              </div>
            </div>
          </div>

          <!-- Educational Conversion Metric -->
          <div class="conversion-widget">
            <div class="metric-circle">
              <span class="metric-val" id="lift-val">+84%</span>
              <span class="metric-lbl">Educational Lift</span>
            </div>
            <div class="metric-info">
              <h4>Doom-Scroll Conversion Rate</h4>
              <p>Replaces passive entertainment decay with high-substance engineering takeaways.</p>
            </div>
          </div>

          <!-- Quick Trap Jump -->
          <div class="trap-shortcut-box">
            <h4>Ready to test the Built-In Trap?</h4>
            <p>See how a shallow keyword system fails vs our latent recommendation agent.</p>
            <button class="btn-primary w-full" id="btn-jump-trap">View Built-In Trap Arena</button>
          </div>
        </div>

      </div>
    </section>

    <!-- TAB 2: BUILT-IN TRAP ARENA -->
    <section id="tab-trap" class="tab-pane">
      <div class="trap-arena-container">
        <div class="arena-header flex-between">
          <div>
            <div class="arena-badge">BENCHMARK SHOWCASE</div>
            <h2>The Built-In Trap: Compound Multi-Reel Session Analysis</h2>
            <p class="arena-desc">
              <strong>The Trap Scenario:</strong> A student watches a sequence of 4 distinct Reels: (1) Java Meme, (2) SWE Lifestyle Vlog, (3) Coding Interview Joke, and (4) Laptop Hardware Comparison.
              A shallow system fails by recommending another generic Java syntax tutorial or sensationalist clickbait ("10 AI tools that will get you a job").
              Our AI Agent discovers the underlying intent: an aspiring Software Engineer exploring real developer workflows, system architectures, and technical interview readiness.
            </p>
          </div>
          <div class="arena-action-btns">
            <button class="btn-primary" id="btn-run-trap-sim">▶ Simulate Full Trap Session</button>
          </div>
        </div>

        <!-- 4 Sequence Reels Cards -->
        <div class="trap-sequence-grid" id="trap-sequence-container">
          <!-- Populated via JS -->
        </div>

        <!-- Head to Head Comparison Grid -->
        <div class="comparison-grid">
          <!-- LEFT: SHALLOW SYSTEM -->
          <div class="comp-col comp-shallow">
            <div class="comp-header">
              <div class="comp-badge badge-danger">SHALLOW KEYWORD BASELINE</div>
              <h3>Naive Keyword Matcher (Fails Trap)</h3>
            </div>
            <div class="comp-body">
              <div class="comp-defect-card">
                <div class="defect-title">❌ Flawed Recommendation 1: Generic Syntax Spam</div>
                <div class="defect-reel">"Java Basics 101: How to Declare an Integer Variable"</div>
                <p class="defect-reason"><strong>Why It Fails:</strong> Pedantic regression. The student is already debugging NullPointerExceptions, not learning basic syntax.</p>
              </div>

              <div class="comp-defect-card">
                <div class="defect-title">❌ Flawed Recommendation 2: Clickbait Hype Trap</div>
                <div class="defect-reel">"10 AI Tools That Will Get You a $200k Software Job in 24 Hours!"</div>
                <p class="defect-reason"><strong>Why It Fails:</strong> Sensationalist clickbait with zero pedagogical value. Hijacks general tech tags without technical rigor.</p>
              </div>

              <div class="comp-verdict verdict-danger">
                VERDICT: FAILED THE TRAP (Keyword spam & hype contamination)
              </div>
            </div>
          </div>

          <!-- RIGHT: OUR AI AGENT -->
          <div class="comp-col comp-agent">
            <div class="comp-header">
              <div class="comp-badge badge-success">OUR AI RECOMMENDATION AGENT</div>
              <h3>Latent Semantic & Anti-Hype Agent (Solves Trap)</h3>
            </div>
            <div class="comp-body">
              <div class="spec-output-card trap-agent-card">
                <div class="spec-field-group">
                  <div class="spec-label">CURRENT REEL:</div>
                  <div class="spec-value highlight-cyan">Session Sequence: [Java NPE Crash Meme] + [Junior Backend Engineer Lifestyle] + [Two-Sum vs Binary Tree Joke] + [M3 vs Snapdragon Thermals]</div>
                </div>

                <div class="spec-field-group">
                  <div class="spec-label">INTEREST DETECTED:</div>
                  <div class="spec-value highlight-amber">Full-Stack Software Engineering, Systems Architecture & Technical Career Readiness</div>
                </div>

                <div class="spec-field-group">
                  <div class="spec-label">WHY:</div>
                  <div class="spec-value text-subtle">The student interacted with 4 interrelated engineering reels: laughing at Java production crashes, admiring PR reviews in a SWE daily routine, engaging with algorithmic interview tension, and analyzing SoC thermal/memory bandwidth limits. This compound signal indicates an ambitious computer science student transitioning from academic syntax into real-world software architecture and career preparation.</div>
                </div>

                <div class="spec-divider"></div>

                <div class="spec-field-group">
                  <div class="spec-label">RECOMMENDED TECH REEL:</div>
                  <div class="spec-value highlight-emerald">"How Instagram Delivers Millions of Reels per Second: CDN Edge Caching & Video Chunking" by ArchitectureExposed</div>
                </div>

                <div class="spec-meta-row">
                  <div class="meta-item"><span class="spec-label">CATEGORY:</span> <span class="meta-pill category-pill">HLD</span></div>
                  <div class="meta-item"><span class="spec-label">DIFFICULTY:</span> <span class="meta-pill diff-pill">Intermediate</span></div>
                  <div class="meta-item"><span class="spec-label">CONFIDENCE:</span> <span class="meta-pill conf-pill">High</span></div>
                </div>

                <div class="spec-field-group">
                  <div class="spec-label">WHY THIS RECOMMENDATION:</div>
                  <div class="spec-value text-subtle">Directly unites their daily social media interaction with enterprise engineering reality. Instead of serving trivial syntax or scammy AI listicles, this recommendation explains large-scale distributed systems, edge CDN caching, and media streaming pipelines—scaffolding their interest toward scalable backend architecture.</div>
                </div>
              </div>

              <div class="comp-verdict verdict-success">
                ✓ VERDICT: SOLVED TRAP WITH HIGH SUBSTANCE & PEDAGOGICAL VALUE
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- TAB 3: CUSTOM REEL SANDBOX -->
    <section id="tab-sandbox" class="tab-pane">
      <div class="sandbox-container">
        <div class="panel sandbox-form-panel">
          <div class="panel-header">
            <span class="panel-tag tag-primary">TEST ARBITRARY REELS</span>
            <h2>Custom Reel Analysis Sandbox</h2>
            <p class="text-subtle">Input any Reel title, transcript, and watch behavior to watch the AI Agent evaluate latent intent and screen for hype in real time.</p>
          </div>

          <!-- Quick Pre-fill Presets -->
          <div class="presets-row">
            <span class="preset-label">Quick Presets:</span>
            <button class="btn-micro" id="preset-btree">Postgres B-Trees</button>
            <button class="btn-micro" id="preset-hype">Clickbait Hype Test ⚠️</button>
            <button class="btn-micro" id="preset-k8s">K8s Pod Crash</button>
          </div>

          <form id="sandbox-form" class="sandbox-form">
            <div class="form-group">
              <label for="sb-title">Reel Title / Hook:</label>
              <input type="text" id="sb-title" class="form-input" required placeholder="e.g. Why PostgreSQL B-Trees are faster than hash tables for range queries">
            </div>

            <div class="form-row">
              <div class="form-group">
                <label for="sb-creator">Creator Handle:</label>
                <input type="text" id="sb-creator" class="form-input" placeholder="@DatabaseMaster">
              </div>
              <div class="form-group">
                <label for="sb-surface-cat">Surface Category:</label>
                <select id="sb-surface-cat" class="form-select">
                  <option value="Coding">Coding</option>
                  <option value="AI">AI</option>
                  <option value="Gaming">Gaming</option>
                  <option value="Gadgets">Gadgets</option>
                  <option value="Career">Career</option>
                  <option value="Programming Memes">Programming Memes</option>
                  <option value="Tech News">Tech News</option>
                  <option value="Entertainment">Entertainment</option>
                </select>
              </div>
            </div>

            <div class="form-group">
              <label for="sb-transcript">Full Transcript / Dialogue:</label>
              <textarea id="sb-transcript" class="form-textarea" rows="3" placeholder="Paste the spoken transcript or voiceover monologue here..."></textarea>
            </div>

            <div class="form-group">
              <label for="sb-visuals">Visual Cues & Tone:</label>
              <input type="text" id="sb-visuals" class="form-input" placeholder="e.g. Whiteboard diagram, memory page splits, serious technical explanation">
            </div>

            <div class="form-row">
              <div class="form-group">
                <label for="sb-watch-rate">Watch Completion: <span id="sb-watch-display">130% (Rewatched)</span></label>
                <input type="range" id="sb-watch-rate" min="0.2" max="2.5" step="0.1" value="1.3" class="slider-input">
              </div>
              <div class="form-group flex-align-end">
                <div class="checkbox-row">
                  <label><input type="checkbox" id="sb-liked" checked> Liked</label>
                  <label><input type="checkbox" id="sb-saved" checked> Saved</label>
                </div>
              </div>
            </div>

            <div class="form-actions">
              <button type="submit" class="btn-primary" id="btn-run-sandbox">Analyze with AI Agent</button>
              <button type="button" class="btn-sm" id="btn-clear-sandbox">Clear</button>
            </div>
          </form>
        </div>

        <div class="panel sandbox-result-panel">
          <div class="panel-header flex-between">
            <div>
              <span class="panel-tag tag-success">LIVE INFERENCE RESULT</span>
              <h2>Agent Output</h2>
            </div>
            <div id="sandbox-hype-badge" class="badge-filter-status">FILTER: READY</div>
          </div>
          <div id="sandbox-output-placeholder" class="spec-output-card">
            <p class="placeholder-text">Submit a custom Reel on the left or select a quick preset to see the AI Agent's latent intent extraction, anti-hype scoring, and structured output.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- TAB 4: TECH REEL CATALOG -->
    <section id="tab-catalog" class="tab-pane">
      <div class="panel">
        <div class="panel-header flex-between">
          <div>
            <span class="panel-tag tag-primary">CURATED REEL BANK</span>
            <h2>Educational Tech Reels Library</h2>
            <p class="text-subtle">Browse all high-substance recommendations scored by the Anti-Hype filter across 9 domains.</p>
          </div>
          <div class="catalog-filters" id="catalog-category-filter">
            <!-- Populated via JS -->
          </div>
        </div>
        <div class="catalog-grid" id="catalog-grid-container">
          <!-- Populated via JS -->
        </div>
      </div>
    </section>

    <!-- TAB 5: FULL REPORT & EXPORT -->
    <section id="tab-export" class="tab-pane">
      <div class="export-container">
        <div class="panel">
          <div class="panel-header flex-between">
            <div>
              <span class="panel-tag tag-primary">EVALUATION REPORT</span>
              <h2>All 8 Sample Reels & Built-In Trap Benchmark</h2>
            </div>
            <div class="btn-group">
              <button class="btn-sm" id="btn-copy-full-report">Copy All Text</button>
              <button class="btn-sm" id="btn-download-md">Download Markdown (.md)</button>
              <button class="bt
