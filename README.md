# Shaune Anotidaishe Bakasa - Profile & Mini-Portfolio

This is my profile and mini-portfolio website built for the Web Technologies module (CIS2103) at Africa University.

The goal was to practice semantic HTML5 and make a simple page that introduces me and shows one of my course projects.

---

## Part C: How I Used AI for the About Section

### 1. The Prompt I Used
I asked the AI to help me write my bio because I was stuck on making it sound professional but not too formal.

**My prompt:**
> Context: I am a Year 2 Computer Information Systems student at Africa University making a portfolio site.  
> Goal: Write a short "About Me" section, 2 paragraphs.  
> Constraints: Sound professional but friendly. Talk about software dev, web tech, and problem solving. Don’t use big words.  
> Format: Just 2 plain paragraphs.

### 2. First Draft from AI
The AI gave me this:
> "I am a driven Computer Information Systems student with a deep passion for software development and web technologies. My academic journey has equipped me with a strong foundation in designing and building modern web solutions that focus on efficiency and seamless user experience.  
> Driven by curiosity and a commitment to continuous learning, I constantly explore emerging frameworks and developer tools. I am dedicated to honing my technical skills and applying technology to solve practical everyday problems."

### 3. What I Changed
I didn’t just copy it. It sounded too much like a CV template.  
So I rewrote it to sound more like me and fit the page better:

**Final version on my site:**
> "I am a dedicated Computer Information Systems student passionate about building efficient, responsive, and user-friendly web applications.  
> Hardworking and curious, I am constantly learning new web technologies and refining my programming skills to solve real-world problems."

I cut out words like "seamless user experience" and "deep passion" because they felt too generic. I wanted it to be short so people actually read it on the homepage.

### 4. What I Learned
Using AI helped me get past writer’s block, but editing it myself made it sound real. Next time I’ll try to write the first draft myself then use AI to improve grammar.

---

## Part D: Accessibility Fix

**Feedback:**  
In Thursday’s practical, my classmate told me my profile image alt text was too vague. I had `alt="Profile photograph"`.

**The problem:**  
That doesn’t tell someone using a screen reader who the photo is of.

**What I did:**  
I changed it to: 
```html
<img src="profile.jpg" alt="Profile photograph of Shaune Anotidaishe Bakasa">



# PROMPT_LOG.md

This file tracks how I used AI while building my portfolio site for CIS2103.

---

### Prompt 1: About Me Bio
**Date:** 09 Sept 2026

**Context:** Year 2 CIS student at Africa University. Building portfolio site. Need an "About Me" section.

**Goal:** Write 2 short paragraphs for the about section.

**Constraints:** Sound professional but friendly. Mention web development and problem solving. Avoid big jargon.

**AI Output:**
"I am a driven Computer Information Systems student with a deep passion for software development and web technologies..."

**What I Changed:**
It sounded too formal and generic. I shortened it to 2 sentences and removed words like "seamless user experience".  
Final version: "I am a dedicated Computer Information Systems student passionate about building efficient, responsive, and user-friendly web applications..."

**What I Learned:**  
AI is good for a first draft, but I need to edit it so it sounds like me.

---

### Prompt 2: Accessibility Fix
**Date:** 09 Sept 2026

**Question to AI:**  
"My peer said my image alt text 'Profile photograph' is too vague. How can I make it better for screen readers?"

**AI Suggestion:**  
"Add who is in the photo and what they are doing. e.g. alt='Profile photograph of Shaune Anotidaishe Bakasa smiling'"

**What I Changed:**  
Updated the `<img>` tag in index.html with the new alt text.

**What I Learned:**  
Alt text should describe the image, not just say "image".

---

### Prompt 3: Debugging CSS
**Date:** 10 Sept 2026

**Question to AI:**  
"I used `<br>` tags to add space between sections. Is there a better way to do this with CSS?"

**AI Suggestion:**  
"Use margin on sections instead. e.g. `section { margin-bottom: 40px; }`"

**What I Changed:**  
Removed `<br><br>` and added margin in styles.css.

**What I Learned:**  
Structure should be HTML, styling should be CSS. Don’t mix them.


# Portfolio Development - Prompt Log

**Developer:** Shaune Anotidaishe Bakasa  
**Project:** Personal Portfolio Website  
**Stack:** HTML5, CSS3, JavaScript  

---

## Log Entries

### [2026-09-11] - Form Refresh Bug & Setup
* **Goal:** Fix page refresh behavior when clicking the "Send" button on the contact form.
* **Prompt:** *"Why is it when I fill in the details of my form it just refreshes?"*
* **Root Cause:** Default form submit behavior reloads the page when the submit button is clicked without `e.preventDefault()`.
* **Resolution:** 
  * Attached event listener to `submit` event on `<form>` instead of `click` on `<button>`.
  * Added `event.preventDefault()` to handle submission via JavaScript cleanly.

---

### [2026-09-11] - Bio & Header Copy Generation
* **Goal:** Craft professional, approachable portfolio copy tailored for recruiters and clients in Zimbabwe/South Africa.
* **Prompt:** Requested 2 bio versions and 3 tagline options following length and keyword constraints.
* **Outcome Selected:**
  * **Tagline:** *"Building fast, responsive websites that grow your business."*
  * **Bio:** Used 3-sentence version highlighting Computer Information Systems background at Africa University, web dev skills, and IT support focus.

---

### [2026-09-11] - Web Development Fundamentals Clarification
* **Goal:** Understand core frontend concepts (`<meta viewport>`, CSS structure, and Semantic HTML).
* **Prompt:** *"Explain to me like I’m new: what does meta viewport actually do... difference between <style> vs external CSS... why use semantic tags over div?"*
* **Key Takeaways:**
  * `<meta viewport>` prevents mobile browsers from rendering desktop-scaled pages.
  * External CSS (`styles.css`) is best practice for clean separation of concerns and caching.
  * Semantic HTML (`<header>`, `<main>`, `<nav>`) improves accessibility (screen readers) and SEO.

---

## Next Action Items
- [ ] Create `styles.css` using CSS Flexbox for modern, responsive layout.
- [ ] Connect contact form to an email handling service (e.g., Formspree/Web3Forms).
- [ ] Add 2 additional student/client project cards in `<main>`.