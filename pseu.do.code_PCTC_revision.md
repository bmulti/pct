# PCTC Document Revision Process including (Handling Out-of-Order Numbers)

0. Verify [PCTC] Marker
   - Search for the marker [PCTC] in the document.
   - If not present, stop the process; this procedure applies only to PCTC documents.

1. Identify Commented Functions
   - Traverse the document and locate all code blocks associated with function definitions.
   - If a function lacks a descriptive comment, add a new comment above the function summarizing its purpose.
   - Ensure all function comments follow the numbering convention of the document.

2. Review Existing Comments and Numbers
   - Locate all comments with numbers according to PCTC rules.
   - Check the sequence of the numbers:
     a) If in order, proceed to step 3.
     b) If out of order, perform the following actions:
        - For each out-of-order comment, insert a new sequential number in front of the code or comment line, followed by the old number.
        - Use the format `<new_number> << <old_number> <comment_text>`.
        - The new number should fit the numbering scheme of the document (e.g., between existing numbers).
        - Log the changes in a separate section of the document or maintain a PCTD record.

3. Assign Numbers to Unnumbered Comments
   - Locate all unnumbered comments in the document.
   - Assign unique numbers using the decimal numbering system:
     a) Insert numbers between existing numbers where necessary.
     b) If no prior numbers exist, start numbering sequentially from 0.01.
   - Ensure numbering respects the sequence of the document and does not overlap.

4. Mark Comments Without Associated Code
   - Identify comments that do not have corresponding code blocks or functions.
   - Retain these comments as annotations, ensuring they remain in the correct sequence with assigned numbers.

5. Finalize Document
   - Recheck the entire document for sequential consistency of numbers.
   - Save the updated document with the renumbering changes clearly indicated and any old numbers preserved.

# Note:
- This approach ensures that historical numbers are preserved for traceability in PCTD while enforcing numbering rules in PCTC.
- The `<<` symbol denotes renumbering and provides clarity on the relationship between the new and old numbers.
