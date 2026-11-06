# Abdul Haseeb — Portfolio

Dark cinematic React + Vite portfolio for **Abdul Haseeb**, focused on AI/ML engineering and software development.

## Included
- Scroll-scrubbed retro-computer hero rendered from optimized WebP frames extracted from the supplied `portfolio video.mp4`.
- Pixel smiley overlay that follows pointer movement within the CRT screen.
- Custom desktop cursor, hidden on touch devices.
- Lenis smooth scrolling, GSAP ScrollTrigger animations, Framer Motion card interactions.
- Responsive Bento-style About section using the supplied sunset, Minecraft, NEFFEX and pixel-art assets.
- Resume-based education, skills, projects and contact information.

## Run locally
```bash
npm install
npm run dev
```
Open the localhost URL shown by Vite.

## Production build
```bash
npm run build
npm run preview
```

## Hero frames
The video is in `public/hero-video.mp4`; 47 WebP frames are in `public/frames/`.
To regenerate them with FFmpeg:
```bash
ffmpeg -i public/hero-video.mp4 -vf "fps=12,scale=1280:-2:flags=lanczos" -c:v libwebp -quality 82 -compression_level 6 -start_number 1 public/frames/frame_%04d.webp
```
If the video or frame count changes, update `FRAME_COUNT` in `src/App.jsx`.

## Before publishing
- Replace LinkedIn and GitHub placeholder destinations in `src/App.jsx` with your real profile URLs.
- Add GitHub links for your projects when available.
- Your uploaded images did not include a personal headshot or audio file, so the portfolio uses the retro computer and visual assets instead of inventing either.
- Confirm whether you want your phone number shown publicly before adding it.

## Stack
React 18 · Vite · Tailwind CSS · GSAP · ScrollTrigger · Framer Motion · Lenis

The static smiley baked into the source video has been removed from the frame sequence so the live cursor-following pixel face can move independently on the CRT screen.
