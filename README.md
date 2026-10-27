# LearnCancer

**Cancer treatment, explained for teens.**

LearnCancer is a website that helps teens understand cancer diagnosis, treatment and side effects through short narrated videos and plain-language answers, because every step is easier when you know what comes next.

Created by **Vedant Arrola** and **Sreeyan Nampally** for the Congressional App Challenge.

> **Not medical advice.** LearnCancer is for education only and does not replace a care team. Always follow the instructions of your oncologist and nurses.

## Who it's for

- Teens (ages 13 to 17) who have cancer
- The family and friends who support them
- English, Spanish and French speakers

## Features

| Page | What it does |
| --- | --- |
| **Home** | A welcome video from UC Davis Children's Hospital, plus slideshows on lessening the impact of cancer and on supporting someone with cancer (arrows, dots, swipe, Start over). |
| **Journey** | Eight steps of treatment: Know Cancer & Staging, Diagnosis, MRI & scans, Ports & IVs, Chemotherapy, Radiation, Side effects, Hospital & home. Each step has a video and three key facts (Facts, Expect, Ask). |
| **Types of Cancer** | Cancers that affect teens, such as leukemia, lymphoma and thyroid carcinoma, with where each starts, common signs and how it's treated. |
| **Get ready** | Two quick questions build a personal checklist for the next doctor visit. The "What to bring", "Questions to ask" and "Ways to cope" tips change with the answers. |
| **About** | Why LearnCancer exists, how it works, and a demo video of the app. |

Other features:
- **Three languages.** The language is picked when the site opens and can be changed any time from the menu at the top. All text and narration switch.
- **Narrated videos.** The Journey videos are slideshows built in the browser from the step's content, with recorded narration in each language.
- **Medical word definitions.** Underlined medical words show a short definition when you hover over or tap them.
- **YouTube videos with custom thumbnails.** Videos from UC Davis Children's Hospital and Princess Margaret Cancer Centre are embedded with credit. Some show a custom thumbnail until clicked.
- **Works on phones and computers.** The layout adapts to the screen size.

## Files

```
LearnCancer/
├── index.html   The website's HTML and JavaScript, including the
│                English, Spanish and French text
├── styles.css   All of the website's styles (CSS)
├── audio/       Narration clips (MP3) for the Journey and welcome videos
├── video/       The About page demo video (MP4 and WebM) and its preview image
└── README.md    This file
```

Keep `styles.css` and the `audio` and `video` folders next to `index.html`. The page loads them by relative path.

## How to run it

**Quick look:** double-click `index.html` to open it in a browser. Everything works except the YouTube videos. YouTube blocks its videos on pages opened from a local file, so clicking a video opens it on YouTube in a new tab instead.

**Full version (recommended):** serve the folder with a local web server, then open the address it prints. For example, with Python installed:

```bash
cd LearnCancer
python3 -m http.server 8000
# then open http://localhost:8000 in a browser
```

**Publishing:** upload the whole folder to any static web host, such as GitHub Pages or Netlify. No build step or server code is needed.

## How it's built

- **HTML** for the page structure.
- **CSS** for the design and the layout on phones and computers.
- **JavaScript** (plain, no frameworks) for page switching, the language system, the narrated video player, the slideshows, the checklist and the definitions.
- **Python** scripts to build the translations and to generate the narration clips with Kokoro, an open-source text-to-speech model.
- **FFmpeg** for audio and video processing, and **Playwright** to test the site in a browser.
- **Claude AI** assisted with developing the code, and with creating, translating and embedding the videos.

## Credits

- Welcome video: UC Davis Children's Hospital (YouTube).
- Know Cancer & Staging and Diagnosis videos: Princess Margaret Cancer Centre (YouTube).
- Medical information is based on public patient resources from the National Cancer Institute (cancer.gov) and the American Cancer Society (cancer.org). Each Journey step links to its sources.

## Review notes

- The medical content should be reviewed by a clinician.
- The Spanish and French translations should be reviewed by native speakers.
