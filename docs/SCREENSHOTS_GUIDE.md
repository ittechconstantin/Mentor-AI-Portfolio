# Authentic Screenshots — Contributor Guide

[← Back to the portfolio](../README.md)

This public repository intentionally ships **without fabricated application screenshots**. You can enrich the portfolio with real images captured from your local Streamlit / FastAPI demo.

## Recommended captures

| Filename to use | Capture | What it demonstrates |
| --- | --- | --- |
| `assets/ai-mentor.png` | AI Mentor response with the **Sources** panel expanded | Agent response grounded in retrieved guides |
| `assets/semantic-search.png` | Semantic Search page with a question and results | Vector retrieval and related guide titles |
| `assets/career-guides.png` | Career Guides page with categorized entries | Practical content browsing |
| `assets/fastapi-swagger.png` | FastAPI Swagger UI showing main endpoints | Backend REST API |

## Before uploading

1. Start the backend and frontend locally and verify the app is working.
2. Use demonstration data only; remove personal information and secret values.
3. Keep all API keys, database URLs, passwords and local file paths out of screenshots.
4. Crop the image so the app interface is readable; avoid large empty areas and browser chrome.
5. Prefer PNG files, clear English interface labels and consistent viewport sizes.
6. Review the captured images before making the repository public.

## Add them to GitHub

1. Open the public portfolio repository.
2. Click **Add file → Upload files**.
3. Drag the real PNG screenshots into the `assets/` folder (or upload from a local copy of the repository).
4. Once the images exist, insert this snippet into `README.md` below “A look at the user experience”:

```markdown
### Real application screenshots

**AI Mentor — retrieved sources and generated response**
![AI Mentor demo](assets/ai-mentor.png)

**Semantic Search — nearest career guides**
![Semantic Search demo](assets/semantic-search.png)

**Career Guides — browsing by category**
![Career Guides demo](assets/career-guides.png)

**FastAPI — interactive API documentation**
![FastAPI Swagger UI](assets/fastapi-swagger.png)
```

**Important:** this guide is not a request to publish the private Python code. Only upload images you have reviewed for sensitive content.

[← Back to the portfolio](../README.md)
