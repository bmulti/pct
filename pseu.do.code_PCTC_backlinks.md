# PCTC Document Backlink Generation Process

0. Verify [PCTC] Marker  
   - Confirm the document contains the marker [PCTC].  
   - If not present, stop the process; this procedure only applies to PCTC documents.

1. Extract Comment Numbers  
   - Parse all comments to identify those with assigned PCTC numbers.  
   - Ignore comments without numbers for this process.  
   - Collect the numbers and associated comments into a structured list for analysis.  

2. Identify Function and Code Relationships  
   - For each function definition or code block, note references to other numbered blocks within the document.  
   - Use static analysis or manually identify where one block calls another.  

3. Generate Backlink Annotations  
   - For each identified reference:
     a) Determine the number of the referenced block.  
     b) Append the backlink in the form `= <referenced_number>` to the referencing comment.  
   - Ensure backlinks are positioned after the main comment text, maintaining PCTC formatting rules.  

4. Order and Validate Backlinks  
   - Backlinks should reflect ascending order of referenced numbers.  
   - Double-check for consistency:
     a) Ensure no duplicate backlinks exist for the same reference.  
     b) Verify that all backlinks point to valid numbers within the same document.

5. Update Document with Backlinks  
   - Insert the generated backlinks into the appropriate comments within the PCTC document.  
   - Save a version of the updated document with all backlinks added.  

6. Optional: Prepare Backlink Map  
   - Create a secondary listing in PCTD format to represent:
     a) The block references in ascending order.  
     b) Reverse mappings to show which blocks are referenced by which numbers.  

# Notes:  
- Backlink additions must follow PCTC rules regarding numbering and formatting.  
- Backlinks do not alter the original meaning of comments; they only add reference metadata.  
- If a backlink references a number from another document, ensure that cross-document linking adheres to PCTD rules.  

# Example Formatting:  
- Original comment:  
  `1.03 Define a helper function to format data`  

- Updated comment with backlink:  
  `1.03 Define a helper function to format data = 1.01`
