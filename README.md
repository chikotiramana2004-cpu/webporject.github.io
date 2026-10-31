# 🏛️ Government Degree College, Khairatabad
## 2nd Year B.Sc (Physical Science) — Student Academic Portal

A modern, fully responsive, and animated educational web portal for college students to view their syllabus, marks distribution, mind maps, and important exam questions.

---

## 📸 Media & Uploaded Asset Integration
All user-provided files have been placed in the `assets/` directory:
- **College Logo:** `assets/khairtabad Logo (2).webp` (Clean circular border, subtle glow, navigation bar branding)
- **Hero Background:** `assets/khairtabad front gate image.jpg` (Full-width hero section with dark gradient overlay and smooth hover zoom)
- **Physics Mind Map:** `assets/physics syllubus mind map.jpg` (Interactive pan/zoom viewer & lightbox modal)
- **Physics Chapters PDF:** `assets/physics chapters.pdf` (Unit-wise marks distribution source & one-click download)
- **Physics Important Questions:** `assets/physics important questions.txt` (36 curated long & short answer questions with topic tags)

---

## 🌟 Key Features & Layout Architecture

### 1. Global Design, Responsiveness & Animations
- **100% Responsive:** Optimized across Mobile, Tablet, and Desktop screens using Tailwind CSS Flexbox/Grid and custom media queries.
- **Mobile Hamburger Navigation:** Collapsible mobile drawer with full subject switching.
- **Animations:** Smooth scroll navigation, fade-up entrance transitions, floating hover effects on cards, and subtle zoom-in on the college gate hero background.
- **Modular Data Architecture:** Data is cleanly structured in `js/data.js` for effortless expansion to Telugu, English, Maths, and Computer Science.

### 2. Header & Top Navigation Bar
- **Left Side:** College circular logo with badge, title *"Government Degree College, Khairatabad"*, and Osmania University affiliation subtext.
- **5 Subject Interactive Buttons:**
  1. `Telugu` (Upcoming / Digitization in Progress)
  2. `English` (Upcoming / Digitization in Progress)
  3. `Maths` (Active: *DSC-III: Differential & Vector Calculus*)
  4. `Physics` (Active: *Paper-III: Electromagnetic Theory*)
  5. `Computer Science` (Active: *Paper-III: Database Management Systems*)
- Clicking on Telugu or English displays a sleek, animated **"Content Coming Soon – Under Update"** card with quick one-click shortcuts to explore Physics, Maths, or Computer Science.
- **Attribution:** Right-side bottom persistent badge and footer imprint: `Design by XVIII.I.XIII.I.XIV.I`.

### 3. Home Page (Hero Section)
- Full-width hero background using `assets/khairtabad front gate image.jpg` with a dark gradient overlay (`rgba(0, 0, 0, 0.65)`).
- Large, bold typography: `"2nd Year B.Sc (Physical Science)"` with fade-up entrance animation.
- Subheading: `"Student Academic Portal: Syllabus, Mind Maps, Marks & Important Questions"`.
- Key stat chips: 4 Units, 80 Marks, Visual Map, 84+ Questions.
- Interactive CTA buttons: *"Explore Subjects"*, *"Interactive Mind Map"*, and *"Exam Questions"*.

### 4. Interactive Subject Dashboards (Physics, Maths & Computer Science)
Each active subject is fully equipped with 3 synchronized sub-tabs:

#### 📑 Tab 1: Syllabus & Marks Distribution
- **Summary Stat Cards:** 4 Units, Teaching Hours (48-60 hrs), 8 Short Questions (Section A), 4 Long Questions (Section B), 80 Total Marks.
- **Responsive Marks Distribution Table:** Unit breakdown, hours, question counts, and 20 marks equal weightage per unit.
- **Detailed Unit Accordions:** Full topic breakdowns, theorems, and learning outcomes for each unit.

#### 🧠 Tab 2: Anti-Blur Vector Mind Maps
- **Pure DOM/SVG Scalable Engine:** 100% crisp, razor-sharp anti-blur rendering at any zoom level (0.4x to 2.5x).
- **Collapsible 4-Level Hierarchy:** Expand/collapse individual branches or use *"Expand All"* and *"Collapse Units"*.
- **Live Search & Auto-Pan:** Real-time search highlighting matching concepts and centering the card.
- **Dedicated Fullscreen Canvas:** Open [mindmap.html](file:///c:/Users/Ramana/Desktop/website/mindmap.html) with top subject-switcher pills (`Physics`, `Maths`, `Computer Science`).

#### ❓ Tab 3: Important Exam Questions & Study Checklist
- **Curated Question Banks:** 84+ total questions across all 3 subjects with 10-Mark Long Questions and Short Answer Questions.
- **Subject-Specific Checklist:** Tracks preparation progress in browser `localStorage` independently for each subject.
- **Filter Toolbar:** Live keyword search, Unit pills (`Unit I` to `Unit IV`), and Type pills (`Long (10M)`, `Short`).

- **Quick Question Actions:** One-click *"Copy Question"* button with toast popup, and print / save as PDF.

---

## 🚀 How to Run the Website

### Option 1: Direct Browser Launch (No Installation Required)
Double-click `index.html` in Windows Explorer or open it with Google Chrome, Microsoft Edge, or Firefox.

### Option 2: Run via Local Dev Server
```powershell
# In the project directory (c:\Users\Ramana\Desktop\website):
npx serve . -l 3000
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🔌 How to Add the Remaining 4 Subjects Later
To add curriculum and question banks for **Telugu, English, Maths, or Computer Science**, simply open `js/data.js`:
1. Find the subject in `ACADEMIC_PORTAL_DATA.subjects`.
2. Set `active: true`.
3. Add the subject data block (similar to `ACADEMIC_PORTAL_DATA.physics`), including its `marksDistribution`, `units`, `mindMapTree`, and `importantQuestions`.
The UI will automatically render the full dashboard for that subject without modifying the HTML or CSS!
