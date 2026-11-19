# Smart Video Ratio Changer

A mobile-friendly, GitHub Pages-ready browser app that converts landscape videos to 9:16.

## Features
- Smart center crop to 9:16
- Blurred background layout that keeps the full original frame visible
- MP4 export, AAC audio, selectable 720p/1080p and 24/30/60 fps
- Processing happens locally in the browser

## Deploy on GitHub
1. Create a new public GitHub repository, for example `smart-ratio-changer`.
2. Upload `index.html` and this `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main`, folder `/ (root)`, then Save.
6. Wait for the Pages URL to appear.

## Important limitations
- This version does **not** use generative AI to invent missing pixels. The "Blur background" mode uses the original video as a blurred backdrop.
- True AI outpainting / subject-aware reframing requires a separate AI video API or a backend service. Never put a private API key in a public GitHub repository or frontend JavaScript.
- Browser-based FFmpeg can be memory-intensive on phones. Try short MP4 clips first. 4K/long videos may fail on some devices.
- The FFmpeg engine is downloaded from jsDelivr on first use, so internet access is required.

## Local testing
You need a local web server because the app uses JavaScript modules. For example:
`python -m http.server 8000`
Then open `http://localhost:8000`.
