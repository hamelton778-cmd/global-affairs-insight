# Global Affairs Insight

A modern, elegant blogging website focused on foreign affairs, international relations, and geopolitical analysis. Built with Next.js 15, TypeScript, and Tailwind CSS with a beautiful dark theme.

## 🌟 Features

- **Modern Design**: Elegant dark theme with responsive layout
- **Blog System**: Dynamic blog posts with categories and featured articles
- **SEO Optimized**: Meta tags, structured data, and semantic HTML
- **Performance**: Built with Next.js 15 and optimized for speed
- **Accessibility**: WCAG compliant with proper contrast and navigation
- **Mobile First**: Fully responsive design that works on all devices

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ 
- npm, yarn, pnpm, or bun

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/global-affairs-insight.git
cd global-affairs-insight
```

2. Install dependencies:
```bash
npm install
# or
yarn install
# or
pnpm install
```

3. Run the development server:
```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

4. Open [http://localhost:3000](http://localhost:3000) to view the website.

## 📁 Project Structure

```
src/
├── app/
│   ├── blog/
│   │   ├── [slug]/
│   │   │   └── page.tsx      # Dynamic blog post pages
│   │   ├── layout.tsx        # Blog layout
│   │   └── page.tsx          # Blog listing page
│   ├── about/
│   │   └── page.tsx          # About page
│   ├── globals.css           # Global styles and Tailwind
│   ├── layout.tsx            # Root layout
│   └── page.tsx              # Homepage
├── components/
│   ├── ui/                   # Reusable UI components (shadcn/ui)
│   ├── Navigation.tsx        # Main navigation component
│   └── Footer.tsx            # Footer component
└── lib/
    └── utils.ts              # Utility functions
```

## 🌐 Deployment Guide

### Step 1: Prepare Your Repository

1. **Initialize Git** (if not already done):
```bash
git init
git add .
git commit -m "Initial commit: Global Affairs Insight website"
```

2. **Create GitHub Repository**:
   - Go to [GitHub](https://github.com) and create a new repository
   - Name it `global-affairs-insight` or your preferred name
   - Don't initialize with README (since you already have one)

3. **Push to GitHub**:
```bash
git remote add origin https://github.com/yourusername/global-affairs-insight.git
git branch -M main
git push -u origin main
```

### Step 2: Deploy with Vercel (Recommended)

1. **Sign up/Login to Vercel**:
   - Go to [vercel.com](https://vercel.com)
   - Sign up with your GitHub account

2. **Import Your Project**:
   - Click "New Project"
   - Import your GitHub repository
   - Vercel will automatically detect it's a Next.js project

3. **Configure Deployment**:
   - Project Name: `global-affairs-insight`
   - Framework Preset: Next.js (auto-detected)
   - Root Directory: `./` (default)
   - Build Command: `npm run build` (default)
   - Output Directory: `.next` (default)

4. **Deploy**:
   - Click "Deploy"
   - Wait for deployment to complete
   - Your site will be live at `https://global-affairs-insight.vercel.app`

### Step 3: Custom Domain Setup (globalaffairsinsight.com)

1. **Purchase Domain**:
   - Buy `globalaffairsinsight.com` from a domain registrar like:
     - Namecheap
     - GoDaddy
     - Google Domains
     - Cloudflare

2. **Add Domain to Vercel**:
   - In your Vercel dashboard, go to your project
   - Click "Settings" → "Domains"
   - Add `globalaffairsinsight.com`
   - Add `www.globalaffairsinsight.com` (optional)

3. **Configure DNS**:
   - In your domain registrar's DNS settings, add these records:
   ```
   Type: A
   Name: @
   Value: 76.76.19.61

   Type: CNAME
   Name: www
   Value: cname.vercel-dns.com
   ```

4. **Verify Domain**:
   - Wait for DNS propagation (can take up to 48 hours)
   - Vercel will automatically issue SSL certificates
   - Your site will be live at `https://globalaffairsinsight.com`

### Alternative: Deploy with Netlify

1. **Sign up to Netlify**:
   - Go to [netlify.com](https://netlify.com)
   - Connect with GitHub

2. **Deploy**:
   - Click "New site from Git"
   - Choose your repository
   - Build command: `npm run build`
   - Publish directory: `out`

3. **Configure for Next.js**:
   - Add `next.config.js`:
   ```javascript
   /** @type {import('next').NextConfig} */
   const nextConfig = {
     output: 'export',
     trailingSlash: true,
     images: {
       unoptimized: true
     }
   }
   module.exports = nextConfig
   ```

### Alternative: GitHub Pages

1. **Install gh-pages**:
```bash
npm install --save-dev gh-pages
```

2. **Update package.json**:
```json
{
  "scripts": {
    "deploy": "gh-pages -d out"
  }
}
```

3. **Configure Next.js for static export**:
   - Add `next.config.js` (same as Netlify config above)

4. **Deploy**:
```bash
npm run build
npm run deploy
```

## 🎨 Customization

### Adding New Blog Posts

1. Edit `src/app/blog/[slug]/page.tsx`
2. Add your post to the `posts` object:
```typescript
"your-post-slug": {
  title: "Your Post Title",
  content: `<p>Your HTML content here...</p>`,
  date: "2024-08-30",
  category: "Your Category",
  readTime: "5 min read",
  author: "Your Name"
}
```

3. Update the posts array in `src/app/blog/page.tsx`

### Styling

- The site uses Tailwind CSS with a custom dark theme
- Colors and spacing can be customized in `src/app/globals.css`
- Component styles use shadcn/ui components

### SEO

- Update metadata in `src/app/layout.tsx`
- Add structured data for better search engine visibility
- Optimize images and add proper alt text

## 🔧 Development

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

### Tech Stack

- **Framework**: Next.js 15
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **UI Components**: shadcn/ui
- **Icons**: Lucide React (when needed)
- **Deployment**: Vercel (recommended)

## 📝 Content Guidelines

### Writing Style
- Professional but accessible tone
- Evidence-based analysis
- Multiple perspectives on complex issues
- Clear structure with headings and subheadings

### Categories
- Geopolitics
- Diplomacy
- Economics
- Security
- Environment
- Regional Studies

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/new-post`
3. Commit changes: `git commit -m "Add new analysis on XYZ"`
4. Push to branch: `git push origin feature/new-post`
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Troubleshooting

### Common Issues

1. **Build Errors**:
   - Check Node.js version (18+ required)
   - Clear node_modules and reinstall: `rm -rf node_modules package-lock.json && npm install`

2. **Deployment Issues**:
   - Verify all environment variables are set
   - Check build logs in Vercel dashboard
   - Ensure all dependencies are in package.json

3. **Domain Issues**:
   - DNS propagation can take up to 48 hours
   - Use DNS checker tools to verify records
   - Contact domain registrar support if needed

### Getting Help

- Check the [Next.js documentation](https://nextjs.org/docs)
- Visit [Vercel's help center](https://vercel.com/help)
- Open an issue in this repository

---

**Global Affairs Insight** - Understanding our interconnected world through expert analysis and insights.
