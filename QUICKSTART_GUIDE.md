# Mintlify Documentation - Quick Start

## Setup in 3 Steps

### 1. Install Mintlify CLI

```bash
npm install -g mintlify
```

### 2. Navigate to Docs

```bash
cd docs/mintlify
```

### 3. Start Local Server

```bash
mintlify dev
```

Visit **http://localhost:3000** to see your documentation!

## Project Structure

```
docs/mintlify/
├── docs.json              # Configuration (navigation, branding)
├── introduction.mdx       # Home page
├── quickstart.mdx         # Quick start tutorial
├── architecture.mdx       # Architecture overview
├── core-concepts/         # Core concepts (6 pages)
├── building/              # Building guides (10 pages)
├── advanced/              # Advanced topics (6 pages)
├── best-practices/        # Best practices (5 pages)
├── deployment/            # Testing & deployment (3 pages)
├── api-reference/         # API docs
└── examples/              # Code examples
```

## Deploy to Mintlify

### Option 1: Mintlify Dashboard (Recommended)

1. Go to https://mintlify.com
2. Sign up / Log in
3. Click "New Documentation"
4. Connect your GitHub repository
5. Set documentation path: `docs/mintlify`
6. Click "Deploy"

Your docs will be live at: `https://your-project.mintlify.app`

### Option 2: Manual Deployment

Push to your GitHub repository and Mintlify will auto-deploy on every commit.

## Customization

### Change Branding

Edit `docs.json`:

```json
{
  "name": "Your Plugin Name",
  "colors": {
    "primary": "#your-color"
  },
  "logo": {
    "dark": "/logo/dark.svg",
    "light": "/logo/light.svg"
  }
}
```

Add logos to `docs/mintlify/logo/` directory.

### Add a New Page

1. Create `your-page.mdx`:

```mdx
---
title: 'Your Page Title'
description: 'Page description'
---

## Content Here

Your content...
```

2. Add to navigation in `docs.json`:

```json
{
  "navigation": {
    "groups": [
      {
        "group": "Your Group",
        "pages": ["your-page"]
      }
    ]
  }
}
```

3. Test locally:

```bash
mintlify dev
```

## Mintlify Components

### Cards

```mdx
<CardGroup cols={2}>
  <Card title="Title" icon="icon-name" href="/path">
    Description
  </Card>
</CardGroup>
```

### Code Groups

````mdx
<CodeGroup>
```javascript JavaScript
const x = 1;
```

```python Python
x = 1
```
</CodeGroup>
````

### Steps

```mdx
<Steps>
  <Step title="First">
    Content
  </Step>
  <Step title="Second">
    Content
  </Step>
</Steps>
```

### Accordions

```mdx
<AccordionGroup>
  <Accordion title="Title" icon="icon-name">
    Content
  </Accordion>
</AccordionGroup>
```

### Callouts

```mdx
<Note>Note content</Note>
<Tip>Tip content</Tip>
<Warning>Warning content</Warning>
<Info>Info content</Info>
<Check>Success content</Check>
```

## Icons

Use Font Awesome or Lucide icons:

```mdx
<Card icon="rocket" />
<Card icon="database" />
<Card icon="code" />
```

Browse icons: https://fontawesome.com/icons

## Documentation Best Practices

1. **Keep it Simple** - Start with clear, concise content
2. **Use Examples** - Always include code examples
3. **Add Diagrams** - Use Mermaid for architecture diagrams
4. **Cross-Reference** - Link related pages
5. **Test Locally** - Preview before deploying

## Need Help?

- **Mintlify Docs**: https://mintlify.com/docs
- **Community**: https://mintlify.com/community
- **Support**: support@mintlify.com

## Common Commands

```bash
# Install CLI
npm install -g mintlify

# Start dev server
mintlify dev

# Check for errors
mintlify check

# Update CLI
npm update -g mintlify
```

## What's Next?

1. ✅ Preview your docs locally
2. ✅ Deploy to Mintlify
3. ✅ Customize branding
4. ✅ Add your logo
5. ✅ Set up custom domain (optional)
6. ✅ Share with your team!

---

**Ready to go!** Your complete documentation is ready to deploy. 🚀
