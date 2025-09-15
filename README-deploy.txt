DEV Blogs - redesigned static site
This folder contains a static redesign of your dev-blogs site.

How to deploy to Vercel:
1. Push this folder to a git repository (GitHub/GitLab).
2. On Vercel, create a new project and import the repository. Vercel will detect it as a static site.
3. Set the "Build & Output Settings" to:
   - Build Command: (leave empty)
   - Output Directory: (root)  [the folder contains index.html already]
Alternatively you can drag & drop this folder into Vercel's static deploy.

What was generated:
- index.html  -> Home page with search and category filter
- posts/slug.md -> original markdown posts (copied)
- posts/slug.html -> per-post pages (render markdown client-side with marked.js)
- posts.json -> metadata used by index
- assets/styles.css -> site styles

Notes & suggestions:
- For SEO and better performance, consider pre-rendering markdown to HTML on a build-time step (I kept client-side rendering to keep the output purely static and simple).
- Add a sitemap.xml and RSS feed (can be generated from posts.json).
- If you prefer a Next.js-based site with server-side rendering / SSG, I can convert this structure to Next.js pages (requires more work).
