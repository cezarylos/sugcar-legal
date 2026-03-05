# SugCar Legal Website

This repository hosts legal/compliance documents for SugCar.

## Files
- `index.html` - Privacy Policy (publish this as GitHub Pages home page)
- `TERMS_OF_SERVICE.md` - Terms of 


## Publish on GitHub Pages

1. Authenticate GitHub CLI:
   ```bash
   gh auth login -h github.com
   ```

2. Create repository and push:
   ```bash
   cd /Users/cezarylos/Documents/sugcar/SugCar/sugcar-legal
   git init
   git add .
   git commit -m "Add SugCar legal documents"
   gh repo create sugcar-legal --public --source=. --remote=origin --push
   ```

3. Enable Pages:
   ```bash
   gh api -X POST repos/cezarylos/sugcar-legal/pages \
     -f source[branch]=main \
     -f source[path]=/
   ```

4. Your policy URL will be:
   - `https://cezarylos.github.io/sugcar-legal/`

Use that URL in App Store Connect Privacy Policy field.
