# AI Usage

Briefly describe how you used AI (tools, prompts, code snippets, fixes). Be concise and honest (using AI is fine; it's 
just a tool; we want to know your method). If you did not use AI, state that here.

Used AI as a support tool:

1. Understanding existing code and writing action comments  
   – Used AI to get line-by-line explanations of the LibraryService class, which helped me understand unfamiliar 
    patterns and decide where changes were needed.
2. Validating my approach  
   – Used AI to check my understanding and identify potential mistakes before implementation.
3. Getting hints
   - Used AI to get hints and guiding questions when I was unsure about the correct approach, to help me think through 
   the solution myself.
4. Working through reservation and handoff logic  
   – Used AI to walk through the reservation-related requirements and service logic step by step, followed the reasoning, 
asked questions, and focused on understanding each part of the solution rather than applying changes blindly.


## Assumptions and Design Decisions

### Return Validation Logic
I implemented the borrower validation logic but kept it disabled. Attempts to enforce this check (including making 
`memberId` mandatory) resulted in application errors and test failures. To follow the assignment requirement of keeping 
the API surface unchanged and to ensure a stable submission, I decided to leave this validation commented out.

### API Response Shape
Although the internal `LibraryService.returnBook` method was updated to return detailed failure reasons, the REST API 
response for `POST /api/return` remains unchanged. This decision was made to follow the assignment instructions regarding 
the API surface, even though the service layer provides more context.
