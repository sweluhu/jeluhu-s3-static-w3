# jeluhu-s3-static-w3
Source code for the personal static website **junioreluhu.com**, hosted on AWS S3.

## Overview

This project is a static website serving as a personal portfolio and gallery. It features a dynamic "E-Mobility" section that showcases various electric vehicles through a responsive image mosaic and video gallery.

## Features

- **Dynamic S3 Integration**: JavaScript logic fetches and parses XML listings from a public S3 bucket to dynamically populate image and video galleries without backend code.
- **Responsive Mosaic Grid**: A custom CSS Grid implementation that arranges images based on their aspect ratio (landscape vs. portrait) to create a visually appealing layout.
- **Custom Lightbox**: A vanilla JavaScript lightbox implementation with:
  - Previous/Next navigation.
  - Keyboard support (Arrow keys, Escape).
  - Touch-friendly controls.
- **Video Gallery**: Auto-playing video thumbnails on hover.
- **Neon Theme**: A distinct dark mode aesthetic with neon green accents.

## Pages

- **Home**: Landing page.
- **E-Mobility**: The main gallery page featuring vehicles like:
  - 2017 BMW i3 Rex Terra
  - 2020 Onyx RCR
  - 2021 Cowboy C4
  - 2024 BMW CE-04
  - 2024 Cake Makka
  - 2025 Tesla Model Y
- **NFT**: NFT Gallery.
- **Fam Bam**: Family photo gallery.
- **Random**: Random image generator.
- **Resume**: Professional resume.

## Tech Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript.
- **Hosting**: AWS S3 (Static Website Hosting).
- **Storage**: AWS S3 (Media assets).


This README was not written a human. It was written by Google Gemini