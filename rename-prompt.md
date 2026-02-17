You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "css/_next_static_chunks_8a80e7184ad3a13f.css",
    "context": {
      "path": "css/_next_static_chunks_8a80e7184ad3a13f.css"
    }
  },
  {
    "path": "css/_next_static_chunks_d2a2aab180e78531.css",
    "context": {
      "path": "css/_next_static_chunks_d2a2aab180e78531.css"
    }
  },
  {
    "path": "imgs/_next_image.webp",
    "context": {
      "refs": [
        {
          "alt": "Logo",
          "title": ""
        },
        {
          "alt": "Logo",
          "title": ""
        },
        {
          "alt": "Engineering the Future of Building and Infrastructure",
          "title": ""
        },
        {
          "alt": "Architecture",
          "title": ""
        },
        {
          "alt": "Logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/about.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/engineers-team.webp",
    "context": {
      "refs": [
        {
          "alt": "Team",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/logo.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/modern-engineering-office.webp",
    "context": {
      "refs": [
        {
          "alt": "Engineering Consultancy",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/why1.webp",
    "context": {
      "refs": [
        {
          "alt": "Engineering Project",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/why2.webp",
    "context": {
      "refs": [
        {
          "alt": "Plan",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Cesource Technical Private Limited",
      "first_heading": "Engineering the Future of Building and Infrastructure"
    }
  },
  {
    "path": "js/_next_static_chunks_3337476739009024.js",
    "context": {
      "path": "js/_next_static_chunks_3337476739009024.js"
    }
  },
  {
    "path": "js/_next_static_chunks_3def03dfd9a8915f.js",
    "context": {
      "path": "js/_next_static_chunks_3def03dfd9a8915f.js"
    }
  },
  {
    "path": "js/_next_static_chunks_66828fa337244043.js",
    "context": {
      "path": "js/_next_static_chunks_66828fa337244043.js"
    }
  },
  {
    "path": "js/_next_static_chunks_69df34fb4c90132b.js",
    "context": {
      "path": "js/_next_static_chunks_69df34fb4c90132b.js"
    }
  },
  {
    "path": "js/_next_static_chunks_6a26f6a70c5d8822.js",
    "context": {
      "path": "js/_next_static_chunks_6a26f6a70c5d8822.js"
    }
  },
  {
    "path": "js/_next_static_chunks_a6dad97d9634a72d.js",
    "context": {
      "path": "js/_next_static_chunks_a6dad97d9634a72d.js"
    }
  },
  {
    "path": "js/_next_static_chunks_b25d10861eeef531.js",
    "context": {
      "path": "js/_next_static_chunks_b25d10861eeef531.js"
    }
  },
  {
    "path": "js/_next_static_chunks_b5b03311248aff00.js",
    "context": {
      "path": "js/_next_static_chunks_b5b03311248aff00.js"
    }
  },
  {
    "path": "js/_next_static_chunks_bcdd8973aa39b992.js",
    "context": {
      "path": "js/_next_static_chunks_bcdd8973aa39b992.js"
    }
  },
  {
    "path": "js/_next_static_chunks_cc1c88799edfe106.js",
    "context": {
      "path": "js/_next_static_chunks_cc1c88799edfe106.js"
    }
  },
  {
    "path": "js/_next_static_chunks_d33560c07053f097.js",
    "context": {
      "path": "js/_next_static_chunks_d33560c07053f097.js"
    }
  },
  {
    "path": "js/_next_static_chunks_f93603dd1e5ce80b.js",
    "context": {
      "path": "js/_next_static_chunks_f93603dd1e5ce80b.js"
    }
  },
  {
    "path": "js/_next_static_chunks_turbopack-5472a641927d3253.js",
    "context": {
      "path": "js/_next_static_chunks_turbopack-5472a641927d3253.js"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.