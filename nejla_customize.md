# How to Customize Your Academic Website
*A Guide for Professor Nejla Asimovic*

Hi Nejla! I've created this guide to help you make changes to your academic website on your own. Everything is already set up and working perfectly - you just need to know where to find things and what to change.

---

## 📚 Table of Contents

1. [Understanding Your Website Structure](#understanding-your-website-structure)
2. [Updating Your About Page](#updating-your-about-page)
3. [Updating Your Research Page](#updating-your-research-page)
4. [Updating Your CV Page](#updating-your-cv-page)
5. [Updating Your Teaching Page](#updating-your-teaching-page)
6. [Customizing Styles, Fonts, and UI](#customizing-styles-fonts-and-ui)
7. [Adding Files (PDFs, Images)](#adding-files-pdfs-images)
8. [Running Your Website Locally](#running-your-website-locally)
9. [Deploying Changes to GitHub](#deploying-changes-to-github)
10. [Troubleshooting](#troubleshooting)

---

## 🏗️ Understanding Your Website Structure

Before we start making changes, let me explain how your website is organized. Think of it like a filing cabinet with different folders for different types of content.

### Main Folders and What They Contain:

| Folder | What's Inside | When You'll Use It |
|--------|---------------|-------------------|
| `_pages/` | All your main website pages | When updating About, Research, Teaching, CV pages |
| `_bibliography/` | Your publications (papers.bib) | When adding new publications |
| `_news/` | News and announcements | When posting updates or news |
| `_sass/` | Colors, fonts, and styling | When changing how things look |
| `assets/` | Images, PDFs, and media files | When adding photos or documents |
| `_config.yml` | Your personal information | When updating name, title, email, etc. |

### How Your Website Works:
1. **Content** (text, images) goes in specific folders
2. **Configuration** (your info) goes in `_config.yml`
3. **Styling** (colors, fonts) goes in `_sass/` folder
4. **GitHub** automatically builds your website when you make changes

### Making Changes - Two Ways:
1. **Through GitHub.com** (I recommend this) - Edit files directly in your browser
2. **On your computer** - If you have the files downloaded locally

---

## 📝 Updating Your About Page

The About page is your homepage - it's the first thing visitors see when they visit your website!

### What You Can Change:
- Your professional bio
- Research interests
- Education background
- Awards and recognition
- News and updates

### Here's How to Update It:

1. **Go to your website repository on GitHub.com**
2. **Click on the `_pages` folder**
3. **Click on `about.md` file**
4. **Click the pencil icon (✏️) to edit**

### Key Sections to Update:

```markdown
---
layout: page
permalink: /about/
title: About
nav: true
nav_order: 1
---

# About Me

Your professional bio goes here. This is what visitors will read first.

## Research Interests

- Your first research interest
- Your second research interest
- Your third research interest

## Education

- **Ph.D.** in [Field], [University], [Year]
- **M.A.** in [Field], [University], [Year]
- **B.A.** in [Field], [University], [Year]

## Awards and Recognition

- Award name, Year
- Another award, Year
```

### My Tips for You:
- Keep your bio professional but accessible
- Update it regularly as your research evolves
- Include recent achievements and news

---

## 🔬 Updating Your Research Page

This page showcases your research work and publications.

### What You Can Change:
- Research interests and focus areas
- Current projects
- Research collaborations
- Publications (automatically generated from your bibliography)

### Here's How to Update It:

1. **Go to the `_pages` folder**
2. **Click on `research.md` file**
3. **Click the pencil icon (✏️) to edit**

### Key Sections to Update:

```markdown
---
layout: research
permalink: /research/
title: Research
nav: true
nav_order: 2
---

# Research

## Research Interests

Brief description of your research focus areas.

## Current Projects

### Project 1: [Project Name]
Description of your current research project.

### Project 2: [Project Name]
Description of another research project.

## Publications

Your publications will appear here automatically based on your `papers.bib` file.
```

### Adding Publications:
Publications are managed in a separate file (`_bibliography/papers.bib`) - I'll show you how to do this in the next section.

---

## 📄 Updating Your CV Page

Your CV page displays your professional experience and qualifications.

### What You Can Change:
- Personal information
- Education history
- Work experience
- Publications
- Awards and honors
- Skills and expertise

### Here's How to Update It:

1. **Go to the `_pages` folder**
2. **Click on `cv.md` file**
3. **Click the pencil icon (✏️) to edit**

### Key Sections to Update:

```markdown
---
layout: cv
permalink: /cv/
title: CV
nav: true
nav_order: 3
---

# Curriculum Vitae

## Education

**Ph.D.** in [Field], [University], [Year]
- Dissertation: [Title]
- Advisor: [Advisor Name]

**M.A.** in [Field], [University], [Year]

**B.A.** in [Field], [University], [Year]

## Academic Appointments

**Assistant Professor**, Georgetown University, [Year] - Present
- McCourt School of Public Policy

## Research Interests

- Computational Social Science
- Digital Technologies
- Intergroup Relations
- Divided Societies

## Publications

[Publications will be automatically generated from your bibliography]
```

### Alternative CV Format:
You can also use a JSON format for your CV by editing `assets/json/resume.json` if you prefer that structure, but I think the markdown format is easier to work with.

---

## 🎓 Updating Your Teaching Page

This page showcases your teaching experience and courses.

### What You Can Change:
- Course descriptions
- Teaching philosophy
- Course materials
- Student feedback
- Teaching awards

### Here's How to Update It:

1. **Go to the `_pages` folder**
2. **Click on `teaching.md` file**
3. **Click the pencil icon (✏️) to edit**

### Adding a New Course:

Here's the format I set up for you - just copy this and customize it:

```markdown
<div class="teaching-item">
  <h3>Course Title</h3>
  <div class="teaching-description">
    Detailed course description here. Explain what students will learn, 
    the course objectives, and any special features.
  </div>
  <div class="teaching-meta">
    <i class="fas fa-calendar-alt"></i>
    <span>Semester - Year</span>
  </div>
</div>
```

### Updating Course Descriptions:

I've already set up custom styling for your teaching page. You can:
- Modify existing course descriptions
- Add new courses using the same format
- Update semester information
- Add course materials or syllabi links

---

## 🎨 Customizing Styles, Fonts, and UI

Now let's make your website look exactly how you want it!

### Changing the Main Color Theme

1. **Go to the `_sass` folder**
2. **Click on `_themes.scss` file**
3. **Click the pencil icon (✏️) to edit**
4. **Find this line and change the color:**

```scss
:root {
  --global-theme-color: #7c4dff;  // Change this color
}
```

### Here are some color options I think would look great:
- **Blue**: `#2196F3`
- **Green**: `#4CAF50`
- **Red**: `#F44336`
- **Orange**: `#FF9800`
- **Purple**: `#9C27B0`
- **Teal**: `#009688`

### Changing Fonts

1. **Go to the `_sass` folder**
2. **Click on `_base.scss` file**
3. **Look for these lines and update them:**

```scss
body {
  font-family: 'Your-Font-Name', 'Roboto', sans-serif;
}

h1, h2, h3, h4, h5, h6 {
  font-family: 'Your-Header-Font', 'Roboto Slab', serif;
}
```

### Here are some font combinations I recommend:
- **Professional**: Roboto + Roboto Slab
- **Modern**: Open Sans + Lato
- **Academic**: Source Sans Pro + Merriweather
- **Clean**: Inter + Playfair Display

### Customizing Teaching Page Styling

I've set up special styling for your teaching page. To modify it:

1. **Go to `_pages/teaching.md`**
2. **Find the `_styles` section at the top**
3. **Modify the CSS to change colors, spacing, or layout**

Example:
```css
.teaching-item {
  background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
  border-left: 4px solid var(--global-theme-color);
}
```

---

## 📁 Adding Files (PDFs, Images)

Now let's add some files to your website!

### Adding PDFs to Your Publications

1. **Go to `assets` folder**
2. **Click on `pdf` folder**
3. **Click "Upload files" and drag your PDF**
4. **Make sure the filename matches what you put in your `papers.bib` file**

### Adding Images

1. **Go to `assets` folder**
2. **Click on `img` folder**
3. **Click "Upload files" and drag your image**
4. **Use the image in your pages like this:**

```markdown
![Description of image](/assets/img/your-image.jpg)
```

### Adding Publications

1. **Go to `_bibliography` folder**
2. **Click on `papers.bib` file**
3. **Click the pencil icon (✏️) to edit**
4. **Add your new publication at the top:**

```bibtex
@article{your2024paper,
  title={Your Paper Title},
  author={Your Name and Co-author},
  journal={Journal Name},
  year={2024},
  pdf={your-paper.pdf},
  abstract={Your abstract here}
}
```

### Supported Publication Fields:
- `pdf` - Link to PDF file
- `code` - Link to code repository
- `website` - Link to project website
- `abstract` - Show abstract on hover
- `selected` - Mark as selected publication

---

## 💻 Running Your Website Locally

Sometimes you want to see changes before they go live. Let me show you how to run your website on your own computer:

### Prerequisites:
- Ruby installed on your computer
- Git installed on your computer

### Steps:

1. **Open Terminal (Mac) or Command Prompt (Windows)**

2. **Navigate to your website folder:**
   ```bash
   cd /path/to/your/website
   ```

3. **Install dependencies:**
   ```bash
   bundle install
   ```

4. **Start the local server:**
   ```bash
   bundle exec jekyll serve
   ```

5. **Open your browser and go to:**
   ```
   http://localhost:4000
   ```

### What This Does:
- Shows you exactly how your website will look
- Updates automatically when you make changes
- Lets you test changes before publishing (which is really helpful!)

### Stopping the Local Server:
- Press `Ctrl + C` in the terminal

---

## 🚀 Deploying Changes to GitHub

Once you're happy with your changes, here's how to make them live on your website:

### Method 1: Through GitHub.com (I recommend this one)

1. **Make your changes** in any file
2. **Scroll to the bottom** of the edit page
3. **Write a brief description** of what you changed
4. **Click "Commit changes"**
5. **Wait 5-10 minutes** for GitHub to update your website

### Method 2: Using Git Commands (Advanced)

1. **Open Terminal/Command Prompt**
2. **Navigate to your website folder**
3. **Add your changes:**
   ```bash
   git add .
   ```
4. **Commit your changes:**
   ```bash
   git commit -m "Description of changes"
   ```
5. **Push to GitHub:**
   ```bash
   git push origin main
   ```

### After Deploying:
- Your changes will appear on your live website
- It may take 5-10 minutes to update
- You can always make more changes and repeat the process (it gets easier each time!)

---

## 🔧 Troubleshooting

Don't worry if something goes wrong - I've got you covered!

### Problem: Changes don't appear on your website
**Solution:** 
- Wait 5-10 minutes, then refresh your website
- Check that you clicked "Commit changes"
- Make sure you didn't get any error messages

### Problem: You see an error message when editing
**Solution:**
- Check that you didn't accidentally delete important symbols like `---` or `{`
- Make sure your text is properly indented
- Click "Cancel" and start over if needed (no worries, it happens to everyone!)

### Problem: Your website looks broken
**Solution:**
- Check that all `---` symbols are still at the top and bottom of files
- Make sure you didn't change any file names
- Try reverting your last change and making it again

### Problem: You can't find a file
**Solution:** 
- Make sure you're in the right folder
- Look for the file name exactly as written (case-sensitive)
- Use the search box in GitHub to find files

### Problem: Local server won't start
**Solution:**
- Make sure Ruby and Git are installed
- Try running `bundle update` first
- Check that you're in the correct directory
- If you're still stuck, don't worry - you can always just use the GitHub method!

---

## ✅ Quick Reference - File Locations

| What You Want to Change | File Location | How to Access |
|------------------------|---------------|---------------|
| Your name, title, email | `_config.yml` | Root folder |
| About page content | `_pages/about.md` | _pages folder |
| Research page content | `_pages/research.md` | _pages folder |
| CV page content | `_pages/cv.md` | _pages folder |
| Teaching page content | `_pages/teaching.md` | _pages folder |
| Publications | `_bibliography/papers.bib` | _bibliography folder |
| News/Updates | `_news/` folder | Create new files here |
| Colors/Theme | `_sass/_themes.scss` | _sass folder |
| Fonts | `_sass/_base.scss` | _sass folder |
| PDFs | `assets/pdf/` folder | assets folder |
| Images | `assets/img/` folder | assets folder |

---

## 🎯 Your Learning Path

Here's the order I suggest you try things:

1. **Start with the About page** - Update your bio and research interests
2. **Add a publication** - Practice with the publications system
3. **Update your teaching page** - Add a new course or update descriptions
4. **Try changing colors** - Experiment with the theme color
5. **Add some news** - Post an update about your research
6. **Test locally** - Set up the local development environment (optional)
7. **Deploy changes** - Make your updates live

---

## 🆘 When You Need Help

### If you get completely stuck:
1. **Revert your changes** - Click "Cancel" and start over
2. **Check this guide again** - Sometimes re-reading helps!
3. **Ask me for help** - I'm here to support you!

### Remember:
- Your website is already set up and working perfectly
- These changes are just about updating content
- You can always undo changes if something goes wrong
- Take your time and don't rush - there's no deadline!

---

*This guide was created specifically for Professor Nejla Asimovic to maintain her academic website independently. I've set everything up for you - now you can focus on updating the content! Feel free to reach out if you need any help.*