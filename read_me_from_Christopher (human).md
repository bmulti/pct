__Ive been shouting at Ai, unruly little buggers very forgetful children, undisciplined so I've invented the PCT__

#PCD has two sections 
## PCTC The coding guidelines and processing
## PCTD The documentation guidelines and processing

Here I've been developing the pseudocode and it is documented in attached files under development. Actually it is not for you, it is for AI to use.
If you want to comment or contribute, note aged and somewhat blind. First programming was with two piles of punch cards. However I am eloquent and write. A site will be online soon at https://mrbmulti.com and hi-ho off we go, can't stop inventing and refining stuff

AI Vomit Attempt i.iiii

This is what AI vomited, theand much detail is qwrong, so you can skip Ai's sales campain for now, it will be updated oneced we have done some more testing

Creating a formal Procedural Code Tree (PCT) guideline document is an excellent idea for systematically managing code complexity and communication. Below is an outline of how PCT can be implemented and refined, followed by examples and suggestions for interaction.

Procedural Code Tree (PCT) Guidelines
Purpose
PCT organizes code into a hierarchical tree of procedures, each uniquely numbered. This system:

Provides clarity on functionality and dependencies.
Facilitates easier debugging and updates.
Encourages better collaboration through consistent documentation.
1. Structure
1.1. Numbering System
Use a hierarchical numbering system:

Main modules: Start with 1.0, 2.0, etc.
Sub-procedures: Add levels, e.g., 1.1, 1.2, 1.2.1.
Floating numbers: Leave room for insertions (e.g., 1.2.1.5 for a later addition).
Revisions: Add revision codes (e.g., 1.2.1.ABC) at the end for tracking updates.

1.2. Naming Conventions
Procedure names should be descriptive but concise.
Include verbs to clarify actions (e.g., FetchRecords, SaveFieldJson).
1.3. Global Constants and Variables
Define and describe global constants/variables at the top level (e.g., 0.1 Constants).
Use structured comments to explain scope, purpose, and dependencies.
2. Documentation
2.1. Embedding in Code
Add comments directly in the code linking to the PCT hierarchy:
python
Copy code
# 1.2.1 Fetch Records
def fetch_records():
    """Retrieves all records from global storage."""
    ...
2.2. Generating Call Logs
Reverse the tree to display calling sequences:
For example, 1.2.1.5 is called by 1.2.1 and 1.2.
Use tools or scripts to generate this view automatically.
2.3. Field List
Maintain a dynamic field list with:
Field name.
Location in the tree.
Responsibility (e.g., purpose, function interaction).
3. Interaction Process
3.1. Planning (Before Coding)
Define functionality using the PCT numbering system in Markdown.
Discuss and finalize tree branches with the user.
3.2. Incremental Updates
Work on one branch/subsection at a time.
Save stable code sections in a separate directory/module.
3.3. User Interaction
Use structured questions to guide discussions:
"Is this hierarchy clear for 1.2.1?"
"Would you prefer additional details for 1.2.1.5?"
3.4. Generating Summaries
Generate summaries of comments, tree structures, or call logs when needed.
4. Examples
4.1. Example Tree in Markdown
markdown
Copy code
## 1.0 Main Module: Record Management
### 1.1 Load JSON
- 1.1.1 Open file.
- 1.1.2 Parse data.

### 1.2 List Records
- 1.2.1 Fetch Records: Retrieves all records from global storage.
- 1.2.2 Render HTML: Displays records in a table.
  - 1.2.2.1 Delete Action: Removes a record.
  - 1.2.2.2 Edit Action: Modifies a record.
  - 1.2.2.3 Copy Action: Duplicates a record.
- 1.2.3 Pagination: Manages page views.

### 1.3 Process JSON Data
- 1.3.1 Update field metadata.
- 1.3.2 Save JSON.
4.2. Embedded Code Example
python
Copy code
# 1.1.1 Open file
def load_json(file_path):
    """Opens a JSON file and loads its content."""
    with open(file_path, 'r', encoding='utf-8') as f:
        return json.load(f)

# 1.2.2.1 Delete Action
def delete_record(record_id):
    """Deletes a record based on its unique identifier."""
    global records
    records = [rec for rec in records if rec["id"] != record_id]
4.3. Reverse Call Log
1.2.2.1 Delete Action
Called by: 1.2.2 Render HTML, 1.2 List Records.
5. Guidelines for Refinement
Ensure all branches and comments are reviewed during discussions.
Allow flexibility for users to insert notes or questions in the hierarchy.
Iteratively improve based on feedback and complexity.
