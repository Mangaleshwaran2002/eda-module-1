---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://picsum.photos/id/58/1900/1080?blur=4
# some information about your slides (markdown enabled)
title: EDA Slides
info: |
  ## EDA (Exploratory Data Analysis) Slides
  Exploratory Data Analysis (EDA) is an approach to analyzing datasets using visual methods to summarize their key characteristics, detect outliers, and uncover patterns before applying machine learning models.
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
author: Mangaleshwaran K
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-up
# enable Comark Syntax: https://comark.dev/syntax/markdown
comark: true
# duration of the presentation
duration: 35min
# used for theme customization, will inject root styles as `--slidev-theme-x` for attribute `x`
themeConfig:
  primary: '#5d8392'
# favicon, can be a local file path or URL
favicon: 'https://faceprep.in/wp-content/uploads/2025/01/FACE-Prep-Site-icon-150x150.png'
# fonts will be auto-imported from Google fonts
# Learn more: https://sli.dev/custom/config-fonts.html
#fonts:
#  sans: Roboto
#  serif: Roboto Slab
#  mono: Fira Code
hideInToc: true

# aspect ratio for the slides
aspectRatio: 16/9

# make canvas take full screen
canvasWidth: 980

addons:
  - excalidraw
  - "@cxphoenix/slidev-addon-python-runner"

# Optional configuration for this runner
python:
  # Install packages from PyPI. Default: []
  installs: ["cowsay","pandas"]

  # Code executed to set up the environment. Default: ""
  prelude: |
    GREETING_FROM_PRELUDE = "Hello, Slidev!"

  # Automatically load the imported builtin packages. Default: true
  loadPackagesFromImports: true

  # Disable annoying warning from `pandas`. Default: true
  suppressDeprecationWarnings: true

  # Always reload the Python environment when the code changes. Default: false
  alwaysReload: false

  # Options passed to `loadPyodide`. Default: {}
  loadPyodideOptions: {}

---

# Exploratory Data Analysis (EDA)

#### By DataScience Mentor | FACEPrep Campus


---
layout: intro
tansition: fade-out
hideInToc: true
---

# Module I: Reproducible Environments & Data Ingestion
By DataScience Mentor | FACEPrep Campus

---
layout: two-cols
layoutClass: gap-16
tansition: fade-out
hideInToc: true
---

# Table of contents

![Table content](https://picsum.photos/500/500)

::right::

<Toc text-xs minDepth="1" maxDepth="2" />


---
src: ./pages/topic-one.md
---

---
src: ./pages/topic-two.md
---

---
src: ./pages/topic-three.md
---

---
src: ./pages/topic-four.md
---

---
src: ./pages/topic-five.md
---

---
src: ./pages/topic-six.md
---

---
src: ./pages/topic-seven.md
---

---
src: ./pages/topic-eight.md
---

---
src: ./pages/topic-nine.md
---

---
src: ./pages/topic-ten.md
---

---
layout: intro
hideInToc: true
---

# Thank you
