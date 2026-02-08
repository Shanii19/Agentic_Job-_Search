# 📸 Application Testing Guide

## Purpose
This guide will help you capture screenshots of all features for documentation.

---

## 🎯 Features to Test & Screenshot

### 1. **Main Job Search Page** (app.py)

**Steps:**
1. Open http://localhost:8501
2. Fill in the form:
   - Job Title: "Software Engineer"
   - Location: "Pakistan"
   - Work Style: "Remote"
   - Minimum Jobs: 10
3. Click "🚀 Launch Agents"
4. Wait for all 3 agents to complete (Memory, Search, Personalization)
5. Scroll down to view job results

**Screenshot to capture:**
- `screenshots/01_job_search_form.png` - The main search form
- `screenshots/02_agents_running.png` - Agents in progress
- `screenshots/03_job_results.png` - Final job listings with bias scores

---

### 2. **Interview Coach - Text Mode** (Pages > Interview Coach)

**Steps:**
1. Click "🎤 Interview Coach" in sidebar
2. Paste a job description (use any Software Engineer JD)
3. Select "Behavioral" question type
4. Choose "5 questions"
5. Select "Text Mode"
6. Click "Generate Questions"
7. View the generated questions
8. Type an answer in the text box
9. Click "Submit Answer"
10. View the AI feedback

**Screenshots to capture:**
- `screenshots/04_interview_setup.png` - Question generation form
- `screenshots/05_text_interview.png` - Text mode interview UI
- `screenshots/06_ai_feedback.png` - Evaluation feedback

---

### 3. **Interview Coach - Voice Mode** (Pages > Interview Coach)

**Steps:**
1. In Interview Coach page, select "Voice Mode"
2. Click "🎤 Start Live Interview"
3. Wait for AI to speak the first question
4. Observe the countdown timer (30s)
5. Click microphone to record
6. Stop recording
7. Wait for transcription
8. View AI feedback

**Screenshots to capture:**
- `screenshots/07_voice_mode_setup.png` - Voice mode selection
- `screenshots/08_live_interview_timer.png` - Countdown timer (30s)
- `screenshots/09_recording_indicator.png` - Recording status
- `screenshots/10_voice_feedback.png` - AI feedback in voice mode
- `screenshots/11_interview_complete.png` - Full transcript at end

---

### 4. **Skill Analysis** (Pages > Skill Analysis)

**Steps:**
1. Click "📚 Skill Analysis" in sidebar
2. Upload a sample resume (PDF/DOCX)
3. Paste a target job description
4. Click "Analyze Skills"
5. View skill gaps
6. View learning roadmap

**Screenshots to capture:**
- `screenshots/12_skill_analysis_form.png` - Upload form
- `screenshots/13_skill_gaps.png` - Identified gaps
- `screenshots/14_learning_roadmap.png` - Recommended courses

---

### 5. **Career Planning** (Pages > Career Planning)

**Steps:**
1. Click "🎯 Career Planning" in sidebar
2. Enter current role (e.g., "Junior Developer")
3. Enter dream role (e.g., "Senior Software Architect")
4. Click "Generate Career Path"
5. View predicted trajectory
6. View bridge roles

**Screenshots to capture:**
- `screenshots/15_career_planning_form.png` - Input form
- `screenshots/16_career_trajectory.png` - Predicted path
- `screenshots/17_bridge_roles.png` - Recommended intermediate roles

---

### 6. **Ethics Dashboard** (Pages > Ethics Dashboard)

**Steps:**
1. Click "🔒 Ethics Dashboard" in sidebar
2. View the bias audit summary
3. Check flagged jobs
4. View audit statistics

**Screenshots to capture:**
- `screenshots/18_ethics_dashboard.png` - Ethics overview
- `screenshots/19_bias_flags.png` - Flagged job listings

---

## 📝 How to Take Screenshots

### Method 1: Windows Snipping Tool
1. Press `Win + Shift + S`
2. Select area to capture
3. Save to `f:\Hackaton\job_search_agent\screenshots\`

### Method 2: Full Screen
1. Press `PrtScn` key
2. Open Paint
3. Paste (`Ctrl + V`)
4. Save to `f:\Hackaton\job_search_agent\screenshots\`

### Method 3: Browser DevTools (Recommended)
1. Press `F12` in browser
2. Press `Ctrl + Shift + P`
3. Type "screenshot"
4. Select "Capture full size screenshot"
5. Save to screenshots folder

---

## ✅ Checklist

After completing all screenshots, verify you have:

- [ ] 01_job_search_form.png
- [ ] 02_agents_running.png
- [ ] 03_job_results.png
- [ ] 04_interview_setup.png
- [ ] 05_text_interview.png
- [ ] 06_ai_feedback.png
- [ ] 07_voice_mode_setup.png
- [ ] 08_live_interview_timer.png
- [ ] 09_recording_indicator.png
- [ ] 10_voice_feedback.png
- [ ] 11_interview_complete.png
- [ ] 12_skill_analysis_form.png
- [ ] 13_skill_gaps.png
- [ ] 14_learning_roadmap.png
- [ ] 15_career_planning_form.png
- [ ] 16_career_trajectory.png
- [ ] 17_bridge_roles.png
- [ ] 18_ethics_dashboard.png
- [ ] 19_bias_flags.png

**Total: 19 screenshots**

---

## 🎨 Tips for Good Screenshots

1. **Full Width**: Zoom out browser to 90-100% to show more content
2. **Clean UI**: Close unnecessary browser tabs/toolbars
3. **Highlight Key Areas**: Use red boxes/arrows if needed
4. **Readable Text**: Ensure text is clear and not blurry
5. **Consistent Size**: Try to keep all screenshots similar dimensions

---

## 📂 After Completion

Once all screenshots are captured:
1. Review each screenshot for clarity
2. Rename any that don't match the naming convention
3. Add them to the README or create a SCREENSHOTS.md file
4. Consider creating a demo video walkthrough

---

**Estimated Time: 15-20 minutes**

Good luck testing! 🚀
