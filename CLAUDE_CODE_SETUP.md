# Claude Code Setup Guide for Tommy's Portfolio

## 🚀 Quick Start

### Step 1: Prerequisites
- Node.js 18+ installed (`node --version`)
- Anthropic API key (get from claude.ai settings)
- Git initialized in your repo

### Step 2: Install Claude Code

```bash
# Install globally
npm install -g @anthropic-ai/claude-code

# Or install locally in your project
npm install --save-dev @anthropic-ai/claude-code
```

### Step 3: Authenticate

```bash
# Set your API key (macOS/Linux)
export ANTHROPIC_API_KEY="sk-ant-..."

# Windows (PowerShell)
$env:ANTHROPIC_API_KEY = "sk-ant-..."

# Or create .env file
echo "ANTHROPIC_API_KEY=sk-ant-..." > .env
```

### Step 4: Verify Installation

```bash
claude-code --version
claude-code --help
```

---

## 💡 Using Claude Code for Your Portfolio

### Basic Syntax

```bash
claude-code "Your task description here"
```

Claude Code will:
1. Read your project files
2. Understand the context
3. Make changes
4. Show you what changed
5. Ask for confirmation before committing

---

## 📋 Pre-Built Commands

We've set up npm scripts in `package.json` for common tasks. Use them like:

```bash
npm run audit
npm run update-materials
npm run add-blog
npm run customize-cv
npm run enhance-ui
```

---

## 🎯 Real-World Examples

### 1. **Audit & Improve Portfolio**
```bash
claude-code "Audit the portfolio website for:
- Performance optimization opportunities
- Accessibility improvements (WCAG compliance)
- SEO enhancements
- Mobile responsiveness issues
Create a report and suggest fixes"
```

### 2. **Add New Features**
```bash
claude-code "Add a dark mode toggle to the portfolio. 
- Use CSS variables for theme switching
- Save preference in localStorage
- Apply to all sections
- Keep the teal and coral color scheme"
```

### 3. **Update Materials Section**
```bash
claude-code "Update the materials section to include:
1. Link to my Medium blog
2. New case study: Lava Network launch
3. Link to GitHub portfolio
4. Testimonials section

Keep the current design style"
```

### 4. **Create Job-Specific Versions**
```bash
claude-code "Create a script that takes a job description as input and:
1. Extracts key requirements
2. Generates a customized CV highlighting relevant experience
3. Creates a cover letter template
Output files as PDF/DOCX

For a SaaS marketing role, create an example output"
```

### 5. **Build Blog Integration**
```bash
claude-code "Create a blog system for the portfolio:
1. Add a /blog page with article listings
2. Create an article template component
3. Add markdown parsing capability
4. Link from portfolio materials section
5. Create 2 sample articles about marketing & Web3"
```

### 6. **Generate Case Studies**
```bash
claude-code "For each project (Lava, Reality+, Genpact, Fujitsu), create:
1. A detailed case study page
2. Metrics and results highlighted
3. Lessons learned section
4. Interactive timeline of the launch
5. Links from main portfolio"
```

### 7. **Integrate Analytics**
```bash
claude-code "Add analytics to the portfolio:
1. Install Plausible or simple analytics
2. Track page views, clicks, conversions
3. Create a simple analytics dashboard
4. Track which materials get clicked most
5. Add heatmap to see where users interact"
```

### 8. **Create API Integration**
```bash
claude-code "Create an API endpoint that:
1. Takes a job description URL or text
2. Uses Claude API to extract requirements
3. Matches against my skills/experience
4. Returns compatibility score
5. Suggests customizations for my CV"
```

---

## 🛠️ Project Structure

After setup, your repo should look like:

```
tommy-portfolio/
├── index.html                 # Main portfolio website
├── package.json              # Dependencies & scripts
├── .env                      # API key (git ignore this!)
├── .gitignore                # Git settings
├── README.md                 # This file
├── assets/                   # Images, icons (if any)
├── styles/                   # Separate CSS (optional)
├── scripts/                  # Utility scripts
│   ├── generate-cv.js        # Job-specific CV generator
│   ├── parse-job.js          # Job description parser
│   └── customize.js          # Personalization script
├── cases/                    # Case studies (if separated)
├── blog/                     # Blog posts (if added)
└── docs/                     # Documentation

```

---

## 🔐 Important: Git Configuration

Add to `.gitignore`:

```
# Environment & API keys
.env
.env.local
*.key

# Dependencies
node_modules/
package-lock.json

# IDE
.vscode/
.idea/
*.swp
*.swo

# Build artifacts (if any)
dist/
build/

# Logs
*.log
npm-debug.log*
```

---

## 📝 Workflow Example

Here's how you'd use Claude Code to improve your portfolio:

```bash
# 1. Initial setup
git clone <your-repo>
cd tommy-portfolio
npm install

# 2. Export API key
export ANTHROPIC_API_KEY="sk-ant-..."

# 3. Ask Claude Code to audit
claude-code "Review the portfolio HTML for:
- Performance issues
- Accessibility
- Mobile responsiveness
- SEO
Suggest improvements"

# 4. Review changes
# Claude Code will show what it wants to change

# 5. Apply changes
# Approve and Claude Code updates your files

# 6. Test locally
npm run dev
# Visit http://localhost:3000

# 7. Commit changes
git add .
git commit -m "Improve portfolio per Claude Code audit"
git push origin main
```

---

## 💻 Advanced: Using Claude Code with Your Job Search

### Create a Job Application Assistant

```bash
claude-code "Create a Node.js script that:
1. Takes a job posting URL or description
2. Uses Claude API to analyze requirements
3. Matches against my experience (Lava, Reality+, etc.)
4. Generates a customized CV from my master CV
5. Creates a cover letter template
6. Suggests which of my case studies are most relevant

Test it with a real SaaS marketing job posting"
```

### Automate Material Updates

```bash
claude-code "Create a script that automatically:
1. Checks my Medium/blog for new posts
2. Updates the portfolio materials section
3. Creates preview cards for new articles
4. Maintains the portfolio design consistency
5. Can be run via npm run update-materials"
```

---

## 🎯 Commands You'll Use Most

```bash
# Just ask Claude Code to do something
claude-code "Your task here"

# Update specific file
claude-code "Update portfolio/index.html to add..."

# Create new feature
claude-code "Create a new page for..."

# Fix issues
claude-code "Debug the mobile responsiveness in..."

# Generate content
claude-code "Create case study for..."
```

---

## 🚨 Troubleshooting

### "Claude Code command not found"
```bash
# Reinstall globally
npm install -g @anthropic-ai/claude-code

# Or use npx to run it without installing
npx @anthropic-ai/claude-code "Your task"
```

### "API key not recognized"
```bash
# Verify your API key is set
echo $ANTHROPIC_API_KEY

# Get a new key from: https://console.anthropic.com/account/keys
# Make sure it starts with "sk-ant-"
```

### "Permission denied"
```bash
# If you get permission errors, try with sudo
sudo npm install -g @anthropic-ai/claude-code

# Or change npm prefix
npm config set prefix ~/.npm-global
export PATH=~/.npm-global/bin:$PATH
```

---

## 📚 Resources

- **Claude Code Docs:** https://docs.claude.com/en/docs/claude-code/overview
- **Claude API Reference:** https://docs.claude.com/en/api/overview
- **Anthropic Docs Map:** https://docs.claude.com/en/docs_site_map.md
- **npm Package:** https://www.npmjs.com/package/@anthropic-ai/claude-code

---

## 🎯 Your Next Steps

1. **Initialize your repo:**
   ```bash
   git init
   npm install
   ```

2. **Add your portfolio HTML file**

3. **Set up API key:**
   ```bash
   export ANTHROPIC_API_KEY="your-key"
   ```

4. **Try your first Claude Code task:**
   ```bash
   claude-code "Review my portfolio and suggest improvements"
   ```

5. **Explore what Claude Code can do!**

---

**Pro Tip:** Start with small tasks and build up. Claude Code is most powerful when it understands your full project context. The more you use it, the better it gets.

Good luck! 🚀
