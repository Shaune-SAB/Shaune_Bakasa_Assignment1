# Shaune Anotidaishe Bakasa - Profile & Mini-Portfolio

This is my profile and mini-portfolio website built for the Web Technologies module (CIS2103) at Africa University.

The project demonstrates semantic HTML5 markup, modern CSS3 styling, CSS Grid and Flexbox layouts, mobile-first responsive media queries, and utility-first styling with Tailwind CSS.

---

## Responsive Notes (Assignment 2 Updates)

### 1. Tested Breakpoints
The page was tested using Chrome DevTools across the three core standard widths to ensure zero horizontal scrolling, overlapping elements, or broken components:
- **Mobile (~375px):** iPhone SE / iPhone 12 Pro (Mobile-first default base layout)
- **Tablet (~768px):** iPad Mini / Portrait Tablet (`min-width: 768px`)
- **Desktop (~1280px):** Standard Laptop / Desktop Monitor (`min-width: 1024px`)

### 2. Flexbox vs. CSS Grid Usage
- **Flexbox (`display: flex`):** Used in the header social links (`.social-links`), navigation drawer/links (`.menu-links`), and experience/project item headers (`.item-header`). Flexbox was selected for these components because they require one-dimensional alignment, dynamic gap management, and horizontal/vertical centering across screen sizes.
- **CSS Grid (`display: grid`):** Used in the **Skills Section** (`.skills-grid`) using `grid-template-columns: repeat(auto-fit, minmax(130px, 1fr))` with `gap: 12px`. CSS Grid was chosen because it creates an automatic multi-column layout that reflows gracefully on small screens without hardcoded breakpoint hacks.

### 3. Tailwind Utility-First Integration
- **Converted Sections:** The **Header Section** and **Contact Form Section** were refactored using Tailwind CSS utility classes.
- **Responsive Variants:** Used responsive variants including `md:p-8`, `md:text-2xl`, `grid-cols-1 md:grid-cols-2`, and `md:w-auto` to scale typography, convert single-column form field rows into multi-column inputs on tablet/desktop, and control button sizing.
- **CSS/Tailwind Architecture Split:** Tailwind CSS is loaded via CDN for rapid form and utility styling, while `style.css` handles core design variables, CSS Grid layouts, custom component transitions, and base mobile-first rules.

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
<img src="profile.jpg" alt="Shaune Anotidaishe Bakasa profile photo">