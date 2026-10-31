CyberShield browser ML deployment

Files:
- index.html: updated website; runs inference in the browser.
- phishing_model.json: trained Multinomial Naive Bayes model required by index.html.

Deploy:
1. Upload/commit both files to the same folder (repository root) on GitHub.
2. Replace the old index.html with this index.html.
3. Keep phishing_model.json in the repository root. If it is already there and unchanged, it can stay.
4. Open the GitHub Pages site over HTTPS and test the Phishing Detector.

The browser loads phishing_model.json with fetch(), so do not open index.html directly as a file.
No Python server or paid backend is required for browser inference.

The model is the existing trained model (122 labelled training samples, 1,374 vocabulary entries).
The training CSV and cybershield.py are not required at runtime. Browser scan counts are session-only.
