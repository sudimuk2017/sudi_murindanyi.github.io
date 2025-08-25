# 📚 Publication Links Update Guide

This guide shows you how to update publication links on your portfolio website.

## 🔗 How to Update Publication Links

### Method 1: GitHub Web Interface (Easiest)

1. **Go to your repository**: https://github.com/sudimuk2017/sudimuk2017.github.io
2. **Click on `index.html`**
3. **Click the pencil icon (✏️)** to edit
4. **Find the publication you want to update** by searching for the title
5. **Replace the `href="#"` with your actual link**

### Method 2: Local Editing

1. **Open `index.html` in any text editor**
2. **Find the publication section** you want to update
3. **Replace the link** and save
4. **Commit and push** changes

## 🎯 Where to Find Publication Links in the Code

### Journal Articles Section
```html
<!-- Search for: Journal Articles -->
<div class="publication-category" id="journals">
    <!-- Your journal publications are here -->
</div>
```

### Conference Papers Section  
```html
<!-- Search for: Conference Papers -->
<div class="publication-category" id="conferences">
    <!-- Your conference publications are here -->
</div>
```

### Preprints Section
```html
<!-- Search for: Preprints -->
<div class="publication-category" id="preprints">
    <!-- Your preprint publications are here -->
</div>
```

## ✏️ Example: Updating a Publication Link

### BEFORE (Template):
```html
<div class="publication-item">
    <div class="pub-content">
        <h4 class="pub-title">Your Paper Title</h4>
        <p class="pub-authors">S. Murindanyi, et al.</p>
        <p class="pub-venue">Journal Name</p>
        <div class="pub-details">
            <span class="pub-year">2024</span>
            <span class="pub-type">Journal</span>
        </div>
    </div>
    <div class="pub-actions">
        <a href="#" class="pub-link" target="_blank" title="View Publication">
            <i class="fas fa-external-link-alt"></i>
        </a>
    </div>
</div>
```

### AFTER (With Real Link):
```html
<div class="publication-item">
    <div class="pub-content">
        <h4 class="pub-title">Your Paper Title</h4>
        <p class="pub-authors">S. Murindanyi, et al.</p>
        <p class="pub-venue">Journal Name</p>
        <div class="pub-details">
            <span class="pub-year">2024</span>
            <span class="pub-type">Journal</span>
        </div>
    </div>
    <div class="pub-actions">
        <a href="https://doi.org/10.1000/your-paper-doi" class="pub-link" target="_blank" title="View Publication">
            <i class="fas fa-external-link-alt"></i>
        </a>
    </div>
</div>
```

**What Changed**: `href="#"` → `href="https://doi.org/10.1000/your-paper-doi"`

## 📋 Common Link Types

### 1. DOI Links (Preferred for Published Papers)
```html
<a href="https://doi.org/10.1000/your-paper-doi" class="pub-link" target="_blank">
```

### 2. ArXiv Links (For Preprints)  
```html
<a href="https://arxiv.org/abs/2401.12345" class="pub-link" target="_blank">
```

### 3. Google Scholar Links
```html
<a href="https://scholar.google.com/citations?view_op=view_citation&hl=en&user=FrYgoaQAAAAJ&citation_for_view=xxx" class="pub-link" target="_blank">
```

### 4. Conference/Journal Direct Links
```html
<a href="https://ieeexplore.ieee.org/document/12345678" class="pub-link" target="_blank">
```

### 5. ResearchGate Links
```html
<a href="https://www.researchgate.net/publication/123456789" class="pub-link" target="_blank">
```

## 🔄 Quick Update Process

1. **Copy your publication link** (DOI, ArXiv, etc.)
2. **Open `index.html`**
3. **Search** for your publication title: `Ctrl+F` or `Cmd+F`
4. **Find the line**: `<a href="#" class="pub-link"`
5. **Replace `#`** with your actual link
6. **Save and commit** changes

## 📝 Adding New Publications

### Step 1: Copy an Existing Publication Block
```html
<div class="publication-item">
    <div class="pub-content">
        <h4 class="pub-title">NEW PAPER TITLE</h4>
        <p class="pub-authors">S. Murindanyi, et al.</p>
        <p class="pub-venue">VENUE NAME</p>
        <div class="pub-details">
            <span class="pub-year">2024</span>
            <span class="pub-type">Journal</span>
        </div>
    </div>
    <div class="pub-actions">
        <a href="YOUR_LINK_HERE" class="pub-link" target="_blank" title="View Publication">
            <i class="fas fa-external-link-alt"></i>
        </a>
    </div>
</div>
```

### Step 2: Update All Fields
- **pub-title**: Your paper title
- **pub-authors**: Author list  
- **pub-venue**: Journal/Conference name
- **pub-year**: Publication year
- **pub-type**: Journal/Conference/Preprint
- **href**: Your publication link

### Step 3: Place in Correct Section
- **Journals**: Add to `<div id="journals">` section
- **Conferences**: Add to `<div id="conferences">` section  
- **Preprints**: Add to `<div id="preprints">` section

## 🚀 Testing Your Changes

### Local Testing:
1. **Start local server**: `python3 -m http.server 8000`
2. **Visit**: `http://localhost:8000`
3. **Click publication links** to test they work
4. **Check mobile responsiveness**

### After Deployment:
1. **Visit**: https://sudimuk2017.github.io/
2. **Test all publication links**
3. **Verify they open in new tabs**

## 🔍 Troubleshooting

### Link Doesn't Work?
- ✅ Check the URL is complete and correct
- ✅ Ensure quotes are properly closed: `href="link"`
- ✅ Verify `target="_blank"` for new tab opening

### Publication Not Showing?
- ✅ Check you're in the right section (journals/conferences/preprints)
- ✅ Ensure proper HTML structure (opening/closing tags)
- ✅ Validate HTML syntax

### Changes Not Appearing?
- ✅ Clear browser cache: `Ctrl+F5` or `Cmd+Shift+R`
- ✅ Wait 5-10 minutes for GitHub Pages deployment
- ✅ Check repository for successful commit

## 💡 Pro Tips

1. **Use DOI links when available** - they're permanent and professional
2. **Keep author formatting consistent**: "S. Murindanyi, et al."
3. **Update publication counts** in the statistics section when adding papers
4. **Test links before committing** to avoid broken links
5. **Use descriptive venue names** rather than abbreviations

## 📊 Updating Statistics

Don't forget to update your publication stats in the summary section:

```html
<div class="pub-stats">
    <div class="stat-item">
        <span class="stat-number">10+</span> <!-- Update this -->
        <span class="stat-label">Total Publications</span>
    </div>
    <div class="stat-item">
        <span class="stat-number">7</span> <!-- Update this -->
        <span class="stat-label">Under Review</span>
    </div>
    <!-- ... other stats ... -->
</div>
```

---

**Need Help?** 
- Check the HTML structure of existing publications as examples
- Test locally before pushing to GitHub
- Keep backups of your working code

Happy publishing! 🎉