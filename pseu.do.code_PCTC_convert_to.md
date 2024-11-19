PCTC Document Conversion Process

0. Do not touch the document with this procedure if it already has [PCTC] in the text.

1. Start with the original document.

2. Initialize a list to hold numbered comments (PCTC comments).

3. Assign a unique number to each comment line, starting from 0.01 and incrementing sequentially for each subsequent comment block:
   - First document: numbers between 0.01 and 0.9999.
   - Each new document gets a unique integer before the decimal point (1, 2, 3, etc.).
   - The numbers after the decimal point can have any fractional value but must be sequential.

4. Insert the comment number at the beginning of each comment:
    - Ensure that the comment number is followed by a space before the actual comment text.

5. Document the rules of the PCTC system in the document header for reference:
    - Include the [PCTC] comment near the top of the document to indicate it follows the PCTC system.

6. If the file name has a number in it, use that number as the document number. Otherwise, make a new number or ask for input based on previous numbers used locally.

7. Final Check:
    - Ensure that all comments are correctly numbered.
    - Verify that all numbers are pure floats and follow the rules of the PCTC system.
