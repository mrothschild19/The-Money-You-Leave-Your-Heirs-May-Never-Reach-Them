# How to Add Blog Posts to Your Website

## Quick Reference

### Adding a New Blog Post

1. **Copy the template:**
   - Duplicate `blog-post-template.html`
   - Rename it (e.g., `my-new-post.html`)

2. **Edit the content:**
   - Change the title in `<title>` and `<h1 class="post-title">`
   - Update the date
   - Write your content

3. **Add to blog index:**
   - Open `index.html` in the blog folder
   - Copy an existing blog post block
   - Paste it at the top of the list
   - Update the title, date, excerpt, and link

---

## Adding YouTube Videos

### Step 1: Get the Video ID

From a YouTube URL like:
```
https://www.youtube.com/watch?v=ABC123xyz
```

The **Video ID** is: `ABC123xyz`

### Step 2: Add the Embed Code

Paste this into your blog post:

```html
<div class="video-container">
    <iframe src="https://www.youtube.com/embed/ABC123xyz" 
            title="YouTube video player" 
            frameborder="0" 
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
            allowfullscreen>
    </iframe>
</div>
<p class="video-caption">Your caption here</p>
```

### YouTube URL Examples

| URL Type | Example | Video ID |
|----------|---------|----------|
| Standard | `https://www.youtube.com/watch?v=dQw4w9WgXcQ` | `dQw4w9WgXcQ` |
| Short | `https://youtu.be/dQw4w9WgXcQ` | `dQw4w9WgXcQ` |
| Shorts | `https://www.youtube.com/shorts/abc123` | `abc123` |
| Live | `https://www.youtube.com/live/xyz789` | `xyz789` |

---

## Full Blog Post Template

```html
<!-- ADD THIS BLOCK to blog/index.html for each new post -->

<div class="blog-post">
    <span class="badge badge-new">NEW</span>
    <h2><a href="YOUR-POST-FILENAME.html">Your Post Title</a></h2>
    <div class="date">Month Day, Year</div>
    <div class="excerpt">A brief description of what this post is about (2-3 sentences).</div>
    <a href="YOUR-POST-FILENAME.html" class="read-more">Read More →</a>
</div>
```

---

## Badge Types

```html
<span class="badge badge-new">NEW</span>      <!-- Blue badge -->
<span class="badge badge-update">UPDATE</span> <!-- Green badge -->
<span class="badge badge-legal">LEGAL</span>   <!-- Orange badge -->
```

---

## After Making Changes

1. **Test locally** - Open the HTML file in your browser
2. **Commit to Git:**
   ```bash
   git add outputs/blog/
   git commit -m "Add new blog post: [your post title]"
   git push
   ```
3. **Wait 1-2 minutes** for GitHub Pages to rebuild

---

## Need Help?

Just ask me to:
- Create a new blog post with specific content
- Add a YouTube video to an existing post
- Create a video gallery page
- Set up automatic posting from a schedule