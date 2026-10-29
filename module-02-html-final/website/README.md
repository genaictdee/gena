# iDigital Concept HTML Foundations Final Project

## Project description

I built a small business website for iDigital Concept to demonstrate the HTML Foundations curriculum. It introduces the business, explains its services, shares short learning articles and includes a practice project application form. I used HTML only. The plain appearance is intentional.

Public project folder: https://github.com/genaictdee/gena/tree/main/module-02-html-final

## Pages included

- index.html — home page, informative figure, ordered process list and fragment link.
- about.html — business introduction, values and purpose of the learning project.
- services.html — a service comparison data table and a description list.
- blog.html — three short articles and links to useful information.
- contact.html — website link, example email link, native audio player and transcript.
- pages/application.html — labelled application form with native validation.

The website folder also contains images, media and this README. The project folder contains screenshots, final validation evidence and browser-checks.json.

## HTML features used

- Complete HTML document structure, English language declaration, UTF-8, responsive viewport metadata and unique page titles and descriptions.
- Header, navigation, main, footer, section, article, address and figure elements.
- Logical headings, paragraphs, strong importance, emphasis, ordered and unordered lists, and a description list.
- Relative links within the same folder, child-folder links to pages/application.html and parent-folder links such as ../index.html.
- Absolute HTTPS links, an email link and same-page fragment links, including a keyboard-accessible skip link.
- An informative SVG image with useful alt text and explicit dimensions, a related figcaption and decorative SVG dots with alt="".
- A real data table comparing service deliverables and business purposes, with a caption, thead, tbody, column headers and row headers with scope attributes. It is not used for page layout.
- Text, email and telephone inputs; a select; radio buttons; checkboxes; a textarea; fieldsets and legends; and a native submit button.
- Visible labels linked to unique control IDs, meaningful names and choice values, required fields, length constraints, an email type constraint and a telephone pattern with help text.
- Native audio controls, a local MP3 source, fallback text, an always-visible download link and a transcript.

## What I learned

I learned that a relative path depends on the folder containing the current page. A top-level page uses pages/application.html to enter the child folder. From the application page, ../index.html returns to the home page.

I also learned that semantic elements explain the purpose of content. Useful alternative text describes an image's purpose, while empty alt is appropriate for decoration. Visible labels and fieldsets make forms easier to understand and use.

## Challenges encountered

The main challenges were keeping navigation consistent, using the correct parent-folder paths, and checking that every form control had a matching label. I also had to distinguish native validation from application processing: HTML can check some input constraints, but this project has no server to store or send applications.

The practice form uses GET and reloads application.html#submission-note with sample values in the URL. The page explains this before the form. Use fictional details only. The submission note is permanent explanatory text, not a claim that an application was received. No passwords, applicant records, keys or private personal media are included.

## Resources and media licences and attributions

Reference documentation consulted:

- W3C Nu HTML Checker: https://validator.w3.org/nu/
- Nu checker project and command-line documentation: https://validator.github.io/validator/
- W3C WAI Images Tutorial: https://www.w3.org/WAI/tutorials/images/
- MDN HTML reference: https://developer.mozilla.org/en-US/docs/Web/HTML

Media:

- images/business-tools.svg and images/dots.svg are original vector illustrations created for this learning project with assistance. They are included locally and may be reused with this submission; no third-party photograph or icon pack was used.
- media/welcome.mp3 is an original project introduction synthesized using FFmpeg and the Flite slt voice. It is not a personal voice recording or voice imitation. Flite software and bundled voice information: https://github.com/festvox/flite . FFmpeg filter documentation: https://ffmpeg.org/ffmpeg-filters.html#flite . The text is supplied in media/welcome-transcript.txt and on the Contact page.
- No external images, music or videos are hotlinked. Documentation links are ordinary external links.

The hello@example.com email address is reserved example data, not an operational business inbox. No working inbox was invented for iDigital Concept.

## Validation evidence

Every final HTML page was submitted directly to https://validator.w3.org/nu/?out=json with Content-Type text/html; charset=utf-8. Each final response reports zero errors and zero warnings. The validation folder contains the original JSON responses, a summary, validation-evidence.md and source SHA-256 hashes tying the evidence to these final files.

## Browser evidence and checks

The screenshots folder contains one full-page browser-rendered screenshot per page. These screenshots show page content without the browser address-bar chrome. The application screenshot contains an empty form, not applicant data.

browser-checks.json records navigation, local resource checks, form constraint checks, audio playback and keyboard skip-link checks. A manual reviewer can also open index.html and use the shared navigation to visit each page.

## How to open the project

Download or clone the project folder. Open website/index.html in a browser and keep the images, media and pages folders in place. No package installation, build step or internet connection is needed for local page navigation and media. External resource links require internet access.

The site was created with assistance for this learning exercise. I should review and understand each HTML feature before presenting it to a mentor.
