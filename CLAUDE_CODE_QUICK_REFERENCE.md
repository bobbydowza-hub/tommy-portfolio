# Claude Code Quick Reference

**Fast lookup for Claude Code commands you can use with your portfolio.**

---

## ⚡ Installation (One-Time)

```bash
npm install -g @anthropic-ai/claude-code
export ANTHROPIC_API_KEY="sk-ant-..."
```

---

## 📋 Basic Pattern

```bash
claude-code "Your request here"
```

Claude Code will:
1. Read your project
2. Make changes
3. Show you what changed
4. Ask for confirmation
5. Commit changes

---

## 🎯 Common Commands

### Portfolio Improvements

```bash
# Audit and optimize
claude-code "Audit the portfolio for performance, accessibility, and SEO. Suggest and implement improvements."

# Add dark mode
claude-code "Add dark mode toggle using CSS variables. Save preference to localStorage."

# Improve mobile
claude-code "Ensure portfolio is fully responsive. Test on all breakpoints. Improve mobile touch targets."

# Add animations
claude-code "Add smooth scroll animations and hover effects throughout the portfolio."

# Accessibility
claude-code "Make portfolio WCAG AAA compliant. Add aria labels, improve contrast, add skip links."
```

### Content & Materials

```bash
# Update portfolio
claude-code "Update the materials section with links to:
- My Medium blog: [url]
- My GitHub: [url]
- My case studies: [folder/url]"

# Add case studies
claude-code "Create detailed case study pages for:
1. Lava Network - Token launch metrics
2. Reality+ - Mobile expansion story
3. Genpact - Digital transformation"

# Create blog
claude-code "Build a blog system that:
1. Parses markdown
2. Shows article listings
3. Supports code highlighting
4. Links from main portfolio"

# Add testimonials
claude-code "Create a testimonials section with quotes from managers, team members, or clients. Include names and roles."
```

### Job Search Automation

```bash
# Generate job-specific CV
claude-code "Create a script (Node.js or Python) that:
1. Takes a job description as input
2. Extracts key requirements
3. Generates a customized CV highlighting relevant experience
4. Outputs as PDF/DOCX

Test with example SaaS marketing role"

# Create application helper
claude-code "Build an interactive form that:
1. Pastes in job description
2. Analyzes my fit
3. Suggests customizations
4. Generates cover letter draft
5. Saves to Notion"

# Job tracker integration
claude-code "Create a script that syncs my job applications to:
1. Notion database
2. Spreadsheet
3. Generates monthly reports
4. Alerts for follow-ups"

# Resume generator
claude-code "Create a tool that generates multiple resume versions:
1. Executive (1 page)
2. Detailed (2 pages)
3. Web3-focused
4. SaaS-focused
5. Enterprise-focused"
```

### Features & Enhancements

```bash
# Add contact form
claude-code "Add a contact form that:
1. Validates email
2. Sends to my email
3. Shows success message
4. Saves to database (optional)"

# Add search
claude-code "Add search functionality to find content on portfolio:
1. Search across sections
2. Highlight results
3. Filter by category"

# Add newsletter signup
claude-code "Add newsletter signup:
1. Email collection
2. Integration with Substack/Mailchimp
3. Confirmation message
4. Privacy compliant"

# Add social sharing
claude-code "Add social share buttons:
1. Share to LinkedIn, Twitter, etc.
2. Custom preview text
3. Tracking (optional)"

# Add comments
claude-code "Add comments section to case studies:
1. Moderate comments
2. Store in database
3. Email notifications"
```

### Analytics & Data

```bash
# Add analytics
claude-code "Integrate Plausible Analytics:
1. Track page views
2. Monitor click events
3. Create dashboard
4. Track conversions"

# Create dashboard
claude-code "Create admin dashboard that shows:
1. Portfolio traffic
2. Most viewed sections
3. User interactions
4. Application clicks"

# Export analytics
claude-code "Create script to export analytics:
1. Monthly reports
2. PDF summaries
3. Email reports automatically"
```

### Advanced

```bash
# Create API
claude-code "Create API endpoint that analyzes job fit:
1. POST: job description
2. Returns: compatibility score
3. Suggests: customizations
4. Generates: cover letter"

# Create bot
claude-code "Create a bot that:
1. Monitors job sites
2. Filters relevant jobs
3. Auto-applies with custom materials
4. Logs everything"

# Create CLI tool
claude-code "Create a CLI tool for managing my job search:
1. claude-code search 'SaaS marketing'
2. claude-code customize cv [job-url]
3. claude-code track [company]
4. claude-code report"

# Deployment automation
claude-code "Create GitHub Actions workflow that:
1. Tests portfolio on push
2. Deploys to Vercel
3. Runs accessibility checks
4. Notifies me of issues"
```

---

## 📦 Using npm Scripts

```bash
# These are pre-configured in package.json
npm run audit              # Audit portfolio
npm run update-materials   # Update materials section
npm run add-blog          # Create blog
npm run customize-cv      # Job-specific CV generator
npm run enhance-ui        # Add new features
```

Each script runs a corresponding Claude Code command.

---

## 🎯 Pro Tips

**1. Be Specific**
```bash
# Good
claude-code "Add a dark mode toggle with these requirements:
- Use CSS variables
- Save to localStorage
- Include keyboard shortcut (Cmd+Shift+D)
- Test all 3 main sections"

# Not as good
claude-code "Add dark mode"
```

**2. One Thing at a Time**
```bash
# Do this
claude-code "Add dark mode"
# Then separately
claude-code "Add search functionality"

# Don't do
claude-code "Add dark mode, search, analytics, and comments all at once"
```

**3. Reference Context**
```bash
# Claude Code reads your files, so you can reference them
claude-code "Update the materials section (around line 250 in index.html) to add Twitter link"
```

**4. Ask for Help**
```bash
# Claude Code can debug its own output
claude-code "The dark mode toggle isn't working. Check the code and fix it."
```

**5. Generate Files**
```bash
# Create new files easily
claude-code "Create a blog post template (blog-template.md) with frontmatter for date, title, author"
```

---

## 🚀 Real-World Workflow Example

```bash
# 1. Start with what you have
git clone <repo>
cd tommy-portfolio
npm install
export ANTHROPIC_API_KEY="..."

# 2. Audit what you have
npm run audit
# Review suggestions
# Approve changes

# 3. Add features
claude-code "Add a testimonials section with 5 placeholder cards"

# 4. Test locally
npm run dev

# 5. Customize for job search
claude-code "I'm applying for a SaaS marketing role. 
Update portfolio to emphasize:
1. Genpact's digital transformation work
2. Fujitsu's B2B campaign success
3. Web3 marketing from Lava experience"

# 6. Deploy
npm run deploy

# 7. Apply with custom materials
claude-code "Generate job-specific CV and cover letter for: [job description]"

# 8. Track in Notion
# Use your job search system to track application
```

---

## ❌ Common Mistakes

**❌ Don't do this:**
```bash
# Too vague
claude-code "Make it better"

# Too much at once
claude-code "Redesign everything, add dark mode, blog, analytics, comments, and API"

# Not specific about output
claude-code "Create something for job search"

# Asking for things outside scope
claude-code "Sell my portfolio for me"
```

**✅ Do this:**
```bash
# Specific and clear
claude-code "Add a dark mode toggle that:
1. Uses CSS variables
2. Stores preference in localStorage
3. Works on all sections
4. Matches teal/coral color scheme"

# One thing at a time
claude-code "Add dark mode toggle"
# Then in next command
claude-code "Create blog system"

# Clear output expectation
claude-code "Create a Node.js script that generates job-specific CVs. Test with sample SaaS job posting."

# Realistic scope
claude-code "Create API endpoint for job fit analysis"
```

---

## 🆘 Troubleshooting

**"Claude Code: command not found"**
```bash
npm install -g @anthropic-ai/claude-code
```

**"API key error"**
```bash
echo $ANTHROPIC_API_KEY
# If empty:
export ANTHROPIC_API_KEY="sk-ant-..."
```

**"Permission denied"**
```bash
sudo npm install -g @anthropic-ai/claude-code
# Or
npm install --save-dev @anthropic-ai/claude-code
```

**"Changes look wrong"**
```bash
# Don't approve! Ask Claude Code to fix it
claude-code "The changes you made don't look right. Here's what's wrong: [describe]. Fix it."
```

---

## 📚 Resources

- **Claude Code Docs:** https://docs.claude.com/en/docs/claude-code/overview
- **Your Setup Guide:** `CLAUDE_CODE_SETUP.md`
- **Your Full README:** `README.md`

---

## 💡 Ideas for Your Portfolio

1. **Make it interactive** - Add animations, hover effects
2. **Track visitors** - See who's looking at your work
3. **Showcase projects** - Add detailed case studies
4. **Collect leads** - Newsletter signup, contact form
5. **Job matching** - API that analyzes job fit
6. **Blog** - Share marketing insights
7. **API** - Let others integrate your portfolio
8. **Mobile app** - Add PWA capabilities
9. **Dark mode** - Style preference
10. **Internationalization** - Support other languages

---

**Start small. Build incrementally. Let Claude Code handle the coding.**

You focus on your job search. Claude Code handles the implementation.

🚀 Happy building!
