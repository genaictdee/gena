# Manual Inspection Before Validation

I inspected the source before sending it to the checker. My initial list was:

1. The html start tag has no lang attribute.
2. The head has no title element.
3. The visible page starts at h3, then skips to h5 for the sections. This is a heading-hierarchy problem even if the validator does not report it.
4. The About link points to pages/about.html, which is not included.
5. The Contact link points to contact-missing, but no element has that ID.
6. A ul is written inside a p. A paragraph cannot contain a list.
7. The explicit closing p after the list has no matching open paragraph after the parser has closed the earlier one.
8. The strong and em elements close in the wrong order.
9. The informative profile illustration has no alt attribute.
10. The ID intro is assigned to two sections.
11. The Name label's for value full-name does not match the input's id name.
12. The email input has no visible associated label.
13. The div opened around the submit button has no closing tag.
14. The fieldset has no closing tag.
15. The second section has no closing tag.

I will also check the local image path, the repaired navigation targets, form keyboard operation and duplicate IDs after repairing the file. HTML validation alone does not verify that relative links point to real files, that descriptions are useful, or that heading choices make sense.

The initial broken.html source is preserved unchanged. Its SHA-256 fingerprint is in validation/source-fingerprints.json.
