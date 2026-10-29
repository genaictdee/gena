# Problem and Fix Table

Line numbers refer to the exact broken.html and fixed.html files included in this project. The malformed original has not been edited.

| Problem | Original location | Repaired location | Fix | Why it matters |
| --- | --- | --- | --- | --- |
| Missing document language | broken.html:2 | fixed.html:2 | Added lang="en" to html. | Helps screen readers choose a pronunciation language. |
| Missing page title | broken.html:3–6 | fixed.html:7 | Added a descriptive title in head. | Identifies the page in browser tabs and assistive tools. |
| Opening heading starts at h3 | broken.html:9 | fixed.html:12 | Changed the page heading to h1. | Establishes the top-level page heading; the original is a hierarchy issue, not automatically invalid HTML. |
| Section headings skip to h5 | broken.html:19 and 27 | fixed.html:22 and 32 | Changed both section headings to h2; the subsection uses h3. | Makes heading relationships understandable. |
| Broken relative page link | broken.html:12 | fixed.html:15 and 21 | Replaced pages/about.html with #about and supplied the matching section ID. | The old path has no destination file; the corrected link reaches the intended section. |
| Broken fragment link | broken.html:13 | fixed.html:16 and 31 | Changed #contact-missing to #contact and supplied that ID. | Allows the link to reach the Contact section. |
| List incorrectly placed inside paragraph | broken.html:20–21 | fixed.html:23–24 | Closed the paragraph before opening ul. | A p cannot contain a ul; browsers otherwise repair the structure automatically. |
| Stray paragraph end tag | broken.html:22 | fixed.html:23–24 | Removed the stray closing p after the list. | The parser has already implicitly closed the earlier p when it sees ul, so this end tag is unmatched. |
| Incorrect strong and em nesting | broken.html:23 | fixed.html:25 | Closed em before closing strong. | Proper nesting closes the inner element before the outer one. |
| Meaningful image has no alt | broken.html:24 | fixed.html:27–28 | Added a useful description and a figure caption; retained dimensions and the valid local image path. | Communicates the illustration’s purpose when it cannot be seen. |
| Duplicate section IDs | broken.html:18 and 26 | fixed.html:21 and 31 | Replaced the repeated intro ID with unique about and contact IDs. | Avoids ambiguous fragment and programmatic references. |
| Name label targets a missing ID | broken.html:31 | fixed.html:38–39 | Changed for="full-name" to for="name" to match the input. | Creates a programmatic label association and makes clicking the label focus the field. |
| Email input has no label | broken.html:32 | fixed.html:42–43 | Added a visible label with for="email". | Gives the control a clear accessible name. |
| Unclosed div | broken.html:34–35 | fixed.html:49 | Removed the unnecessary div and used a closed paragraph around the button. | Restores balanced containment at the form end. |
| Unclosed fieldset | broken.html:29–35 | fixed.html:35–50 | Added the closing fieldset before closing form. | Keeps the group of related controls correctly contained. |
| Unclosed second section | broken.html:26–36 | fixed.html:31–56 | Closed the Contact section before closing main. | Restores a properly nested main content structure. |

## How the problems were found

manual-diagnosis.md records the source inspection. The initial W3C report contains 10 errors and one warning. It identifies the missing title and alt, duplicate IDs, paragraph and emphasis nesting errors, and unclosed div and fieldset elements. One error is a fatal stop at line 35, so the checker explicitly says that further errors are ignored. Its one warning points to the first occurrence of the duplicate ID; it is not a language warning. Missing language, label associations, the unclosed section, heading order and broken destinations are documented from manual inspection and browser checks even when absent from this initial truncated diagnostic run. A clean final checker result alone does not prove link availability or useful descriptions.

## Additional improvements

The corrected page also includes a description meta tag, named navigation, a skip link, visible required-field instructions and native form constraints. These improve clarity and usability; they are not all claims that the original was syntactically invalid. The original doctype, character encoding, viewport metadata and native submit button were already present and were retained.

## Media attribution

images/profile.svg is original generic vector artwork created for this exercise with assistance. It is not a private photograph or a likeness of a real person. No external asset is hotlinked.
