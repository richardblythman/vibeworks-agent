# Claude Code Workshop Guide

A hands-on guide to building a website with Claude Code and AI assistance.

---

## 1. Folder Structure

Set up your project workspace:

```
Desktop/
└── Project/
    ├── PRD.md
    └── Website.zip
```

### Setup Instructions

1. **Create a Project folder** on your Desktop
2. **Download [PRD.md](./PRD.md)** and place it in the folder
3. **Get a website template**
   - Go to [v0.app/templates](https://v0.app/templates)
   - Download any template that interests you
4. **Add to your project** and unzip the Website.zip file

---

## 2. Open Claude Code

### Get Started in 4 Steps

**Step 1: Open Terminal**
- Mac/Linux: Terminal
- Windows: PowerShell

**Step 2: Navigate to Your Project**
```bash
cd ~/Desktop/Project
```

**Step 3: Start Claude Code**
```bash
claude
```

**Step 4: Brief Claude**
```
Understand all of the files here
```

---

## 3. Build the Website

### The Main Prompt

Ask Claude to build your website with this prompt:

```
Build me a website using the website template. Use PRD.md as the instructions
for what to build. Run it locally when you're done.
```

### What Claude Will Do

- 📖 Read and understand the [PRD.md](./PRD.md) requirements
- 🎨 Apply the color scheme and styling
- 🏗️ Build all the sections (Hero, Features, Team, Contact)
- 📝 Create the contact form
- 🚀 Run `npm run dev` to start the local server

---

## 4. View Your Website

Once Claude finishes building, you'll see:

```
$ npm run dev

VITE v5.0.0 ready in 500 ms

➜ Local: http://localhost:3000
```

**To view your site:**
- Option 1: Ctrl + Click the link in terminal
- Option 2: Copy the URL and paste it in your browser

---

## 5. Change the Look

### Customize with Components

Browse pre-built components to enhance your website design.

**How to Find Components:**

1. **Browse Components**
   - Visit [21st.dev/community/components](https://21st.dev/community/components)
   - Preview pricing tables, maps, testimonials, footers, and more

2. **Find What You Like**
   - Click on components to preview them in action

3. **Copy the Prompt**
   - Click "Copy Prompt" to copy component details to your clipboard

4. **Paste into Claude**
   - Share the copied prompt with Claude to add it to your website

### Example Prompt

```
I want a pricing section like this: [paste copied prompt]
```

### Ideas to Try

- 💰 Pricing Tables
- 🗺️ Maps
- ⭐ Testimonials
- 📊 Stats
- 🦶 Footers
- 🎯 CTAs (Call-to-Action buttons)

---

## 6. Add SEO Skill

### Optimize for Search Engines

1. **Download the SEO Skill**
   - Download SEO-SKILL.md

2. **Add to Your Project**
   - Save SEO-SKILL.md in your Project folder

3. **Import the Skill**
   ```
   Import SEO-SKILL.md as a skill
   ```

4. **Run SEO on Your Website**
   ```
   Run the SEO skill on my website
   ```

### What Claude Will Add

- 🏷️ Meta tags (title, description, keywords)
- 📱 Open Graph & Twitter Cards for social sharing
- 📊 Structured data (JSON-LD schemas)
- 🤖 AI search optimization (Quick Answer, FAQ)
- 🗺️ Sitemap and robots.txt

---

## 7. Share Your Experience

### Use the Social Media Agent

Turn your workshop experience into engaging posts across all platforms.

**Setup:**

1. **Download the Agent**
   - Download SOCIAL-MEDIA-AGENT.md

2. **Add to Your Project**
   - Save SOCIAL-MEDIA-AGENT.md in your Project folder

3. **Import the Agent**
   ```
   Import SOCIAL-MEDIA-AGENT.md as a subagent
   ```

4. **Verify Setup**
   ```
   /agents
   ```
   You should see your social-media agent listed

5. **Create Your Post**
   ```
   Use the social media agent to create a LinkedIn post about my
   experience at the Claude Code workshop today. I built a website using AI!
   ```

6. **Share It!**
   - Copy the generated post and share on your preferred platform

**Works With:**
- 💼 LinkedIn
- 𝕏 Twitter/X
- 📸 Instagram
- 📘 Facebook
- 🧵 Threads

---

## 8. Sync to GitHub (Optional)

### Back Up Your Code

Save your project to GitHub for version control and cloud backup.

**Ask Claude:**
```
Sync this project to my GitHub repo https://github.com/username/my-website
```
*(Replace with your actual GitHub repo URL)*

**Claude Will Handle Everything:**
- 📂 Initialize a git repository
- 📝 Create a .gitignore file
- ☁️ Create a GitHub repository
- 🚀 Push all your code

---

## 9. Deploy to the Internet (Optional)

### Go Live with AWS

Put your website on the real internet for everyone to see.

**Ask Claude:**
```
Deploy this website live to my domain example.com using the AWS CLI.
Set up S3 hosting and configure everything needed.
```
*(Replace example.com with your actual domain)*

**Claude Will Do:**
- 📦 Build your website for production
- 🪣 Create an S3 bucket
- ⬆️ Upload your files
- 🌐 Configure public hosting
- 🔗 Give you a live URL

**Your website will be live at:**
```
https://example.com
```

---

## 10. Create a Visual Map (Optional)

### Visualize Your Website

Create an Obsidian canvas showing all the features of your site.

**Ask Claude:**
```
Create an Obsidian canvas that maps out all the features of my website
```

**Claude Will Create:**
- 🎨 Visual nodes for each page/section
- 🔗 Connections showing relationships
- 📊 Feature groupings and hierarchy
- 🗂️ A .canvas file ready to open in Obsidian

---

## 🎉 You Did It!

You just built a website with AI!

**Next Steps:**
- Share your experience on social media
- Get feedback from the community
- Iterate and improve your design
- Show your friends what you built

---

## Tips for Success

- **Start simple**: Build the basics first, then add features
- **Ask clearly**: The more specific your prompts, the better Claude's results
- **Iterate**: Use the component library to refine your design
- **Get feedback**: Share your site with the community and gather ideas
- **Have fun**: Experiment with different templates and components

Now go build something amazing! 🚀
