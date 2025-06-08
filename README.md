# Markdown & LaTeX Document Creator

![made-with-html-css-js](https://img.shields.io/badge/Made%20with-HTML%2C%20CSS%2C%20%26%20JS-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

A single, self-contained HTML file that acts as a powerful client-side renderer for Markdown and LaTeX. Perfect for students, educators, and researchers who need to quickly create and share beautifully typeset documents without any server-side dependencies or complex software installations.

---

### Video


https://github.com/user-attachments/assets/bdaf5b88-fc7e-4aa8-bc13-8ac2c83dd934


---

### Free Online Version

You can use it right now:
<a href="https://lab.dekraker.dev/text-to-latex/">https://lab.dekraker.dev/text-to-latex/</a>

---

## ✨ Features

*   **Client-Side Rendering:** All processing happens directly in your browser. No data is sent to any server, ensuring privacy and offline functionality.
*   **Dual Input Methods:**
    *   **File Upload:** Click "Choose File" to load a local `.txt` or `.md` file.
    *   **Manual Paste:** Use the collapsible text area to paste content directly.
*   **Rich Document Export:**
    *   **Print:** A clean, print-optimized stylesheet hides the UI for a professional hard copy.
    *   **Save as PDF:** Generate a high-quality, downloadable PDF of your rendered notes with a single click.
*   **Light & Dark Modes:** A sleek theme-switcher with sun/moon icons allows you to toggle between light and dark modes. Your preference is automatically saved in your browser's local storage.
*   **Zero Installation:** The entire application is a single HTML file. Just download and open it in any modern web browser.

---

## 🚀 How to Use

1.  **Download:** Get the `document_creator.html` (or similarly named) file from this repository.
2.  **Open:** Double-click the file to open it in your web browser (e.g., Chrome, Firefox, Safari, Edge).
3.  **Input Content:**
    *   Click the **"Choose File"** button to load a local `.md` or `.txt` file.
    *   OR, click **"Or Paste Text Manually"**, paste your content into the text area, and click **"Render Pasted Text"**.
4.  **Export:** Once your document is rendered, use the **"Print"** or **"Save as PDF"** buttons that appear at the top of the content area.

---

## 🛠️ Technologies Used

This project is a great example of a powerful front-end-only application.

*   **Core:** HTML5, CSS3 (with CSS Variables for theming), and Vanilla JavaScript.
*   **Math Typesetting:** [MathJax](https://www.mathjax.org/) - For beautifully rendering LaTeX equations.
*   **PDF Generation:** [html2pdf.js](https://github.com/eKoopmans/html2pdf.js/) - For client-side HTML-to-PDF conversion.
*   **Icons:** [Font Awesome](https://fontawesome.com/) - For clean, scalable UI icons.

---

## 🔧 How It Works

1.  **Parsing:** A simple, custom JavaScript function parses the input text. It recognizes basic Markdown syntax (headings, lists, bold text, horizontal rules) and converts it into corresponding HTML tags. LaTeX blocks (`$...$` and `$$...$$`) are left untouched.
2.  **Rendering:** The generated HTML is injected into the main content area of the page.
3.  **Typesetting:** The MathJax library is then invoked to scan the new content and transform all LaTeX blocks into high-quality, SVG-based mathematical notation.
4.  **Theming:** Light and dark modes are handled efficiently using CSS Variables. A `data-theme` attribute on the `<html>` tag toggles between two sets of color variables, and the user's choice is persisted via `localStorage`.
5.  **Exporting:**
    *   The "Print" button triggers the browser's native print dialog, using a special `@media print` stylesheet to format the output.
    *   The "Save as PDF" button uses the `html2pdf.js` library to capture the rendered HTML content (including the SVG math) and compile it into a PDF file for download.

---

## ⚖️ License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
