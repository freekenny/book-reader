# Web Book Reader

A lightweight, client-side, minimalist web application for reading **PDF** and **EPUB** books directly in the browser. 

Designed with simplicity in mind, this reader runs entirely in the browser without any server-side requirements, heavy databases, or complex configurations.

## Key Features

*   **Minimalist & Single-File Design**: Built using pure HTML, CSS, and JavaScript. Zero installation, zero external dependencies to manage.
*   **Dual Format Support**: Reads both PDF and EPUB files seamlessly.
*   **Dynamic Page Indicator**: Displays the current page dynamically at the top center of the screen, adjusting seamlessly between double-page spreads on desktop and single-page layouts on mobile.
*   **Table of Contents Extraction**: Automatically parses outline headers for PDFs and navigation files for EPUBs to generate an interactive sidebar for chapters.
*   **Quick Navigation**: Skip to specific pages instantly using a simple page input form.
*   **Offline-Ready**: Once downloaded, it can run completely offline (provided the library scripts are loaded/cached).

## How to Run

Because modern browsers enforce Security/CORS policies, loading EPUB files from a local file path (`file://`) will fail. To use this application, you must run it via a local web server:

### Option 1: Python (Quickest)
If you have Python installed, open your terminal/command prompt in this folder and run:
```bash
python -m http.server 8000
```
Then visit `http://localhost:8000` in your browser.

### Option 2: VS Code Live Server
If you use VS Code, install the **Live Server** extension, open the project folder, and click the **Go Live** button in the bottom status bar.

### Option 3: Node.js (http-server)
If you have Node.js installed:
```bash
npx http-server -p 8000
```
Then visit `http://localhost:8000`.

## Libraries Used
*   [PDF.js](https://mozilla.github.io/pdf.js/) for client-side PDF rendering.
*   [epub.js](https://github.com/futurepress/epub.js/) for client-side EPUB rendering and navigation.
*   [JSZip](https://stuk.github.io/jszip/) (dependency of epub.js) to extract EPUB containers.
