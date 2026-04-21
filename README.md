# Build-with-MeDo-Hackathon

## Text Description

### 1. The Problem:

Product return is something that d small e-commerce store owners handle almost on a daily basis. Yet, most of them have no system to make sense of their returns. They are overwhelmed one-line customer notes 'doesn't fit, ' 'not what I expected, ' 'arrived broken' and have no way to detect patterns or to decide where to focus first. The idea of ReturnRadar came to me as a solution to this: you paste your raw return reasons, and you end up with a ranked breakdown, root cause analysis, and a supplier-ready action plan.

### 2. How I Structured My Conversations with MeDo:

I began with a simple concept and a problem statement, then entrusted MeDo with doing the in-depth thinking. To me, my initial prompt was pretty much: "I want to build a web app for small e-commerce owners to analyse product return reasons and get actionable recommendations." After that, MeDo assisted me to turn the idea into a complete product, by producing a comprehensive requirements document spanning all five pages of the app (Landing, Input, Processing, Results Dashboard, and Report), including the business logic, edge cases, and acceptance criteria.

That requirements document served as the plan for MeDo to develop the app. I went through it page by page in subsequent conversations, sending each section to MeDo, explaining the desired behaviour, examining the output, and making the necessary modifications. The idea that MeDo first wrote the spec and then built from the spec within the same workflow was an entirely new mode of working for me.

### 3. The Most Impressive Feature MeDo Generated:

The Results Dashboard actually got right to the core of the matter, delivering a dramatic upswing in execution and efficacy. Beginning with a mere brief, MeDo drafted an interactive donut chart that visualized the five categories of return, alongside a red Priority Fix badge that intuitively highlights the worst-contributing factor, severity bars ranked by percentage share and color-coded, root-causes diagnostics per category, and three specific highly-targeted fixes per each problem, for example, "adding a size comparison chart with brand-specific versus standard sizing" and "updating your supplier QC checklist with specific quality checkpoints."

Moreover, what made it truly remarkable was that MeDo didn't just furnish the presentation of the content it even connected the logic. The Priority Fix badge is following the correct tie-breaking order (sizing -> quality -> expectation mismatch -> shipping damage -> wrong item), cost estimates show up only when refund value is provided, and the entire dashboard is dynamically populated from whatever return data the user submits.

### 4. The AI Classification Engine:

ReturnRadar's primary feature is an AI-powered system that analyses raw, disorganised reasons for returns and matches each one to the most appropriate of the five predefined categories. Customers do not have to sort or label their data beforehand as they simply copy and paste the messy, real-life notes of customers and the AI takes care of everything, it calculates percentage shares as well as gives back a prioritised ranking within a few seconds.
The Report Page

A feature that's really close to my heart is the shareable report. MeDo created a neat, very professional summary page with the store name editable field; date of analysis, total returns count, top 3 issues with their specific fixes and an estimated monthly savings figure are all auto filled. Copy to Clipboard and Download PDF work straight away so a store owner can carry out an analysis and get the results off to their supplier within minutes.

### 5. The Result:

It is a fully deployed, no-login-required web app that any small store owner can use in less than two minutes. It converts a messy stack of return notes into a clear, organised to-do list and a document that one can effectively send to a supplier.

## Requirements Document

### 1. Application Overview

#### 1.1 Application Name
ReturnRadar

#### 1.2 Application Description
ReturnRadar is a web application designed for small e-commerce store owners to analyse product return reasons, identify patterns, and receive actionable recommendations to reduce preventable returns. The app processes return data through text input or file upload, categorises return reasons, and generates a comprehensive analysis report with cost estimates and improvement suggestions.

### 2. Users and Use Scenarios

#### 2.1 Target Users
Small e-commerce store owners who need to understand and reduce product return rates.

#### 2.2 Core Use Scenarios
- Analyse return reasons from customer feedback or return forms
- Identify the most common return categories and their impact
- Receive specific actionable recommendations to reduce returns
- Estimate the financial impact of preventable returns
- Generate and share analysis reports with suppliers or team members

### 3. Page Structure and Functionality

#### 3.1 Page Structure
```
ReturnRadar
├── Landing Page
├── Input Page
├── Processing Page
├── Results Dashboard
└── Report Page
```

#### 3.2 Landing Page

**Page Purpose**: Introduce the application value and guide users to start analysis.

**Page Elements**:
- Headline introducing ReturnRadar
- Value proposition explaining how the app helps reduce returns
- Analyse My Returns CTA button

**Functionality**:
- Click Analyse My Returns button navigates to Input Page

#### 3.3 Input Page

**Page Purpose**: Collect return reason data from users.

**Page Elements**:
- Large text area for pasting return reasons (primary input method)
- CSV or TXT file upload option
- Optional field for average refund value in dollars
- Submit button to start analysis

**Functionality**:
- Users can paste return reasons directly into the text area, one reason per line
- Users can upload a CSV or TXT file containing return reasons, one per line
- Users can optionally enter average refund value to enable cost estimation
- Click Submit button validates input and navigates to Processing Page
- At least one input method (text area or file upload) must contain data before submission

#### 3.4 Processing Page

**Page Purpose**: Provide visual feedback while analysing return data.

**Page Elements**:
- Animated loading indicator
- Text message: Analysing your returns...

**Functionality**:
- Display animated loading state while processing return data
- Automatically navigate to Results Dashboard when analysis completes

#### 3.5 Results Dashboard

**Page Purpose**: Display comprehensive analysis results with actionable insights.

**Page Elements**:
- Donut chart showing the breakdown of return categories with percentage shares
- Red Priority Fix badge displayed on the category with the highest percentage
- Ranked list of return categories with the following information for each:
  - Category name: sizing, quality, expectation mismatch, shipping damage, wrong item
  - Percentage share of total returns
  - Colour-coded severity bar indicating impact level
- For each category:
  - Root cause diagnosis
  - 3 specific actionable fixes
- Total estimated monthly cost of preventable returns (displayed if average refund value was provided)
- Download Report button

**Functionality**:
- Display donut chart visualising the percentage breakdown of all five return categories
- Highlight the category with the highest percentage share with a red Priority Fix badge
- Display return categories ranked by percentage share from highest to lowest
- Use colour-coded severity bars to visualise impact (higher percentage = higher severity)
- Show root cause and actionable recommendations for each category
- Calculate and display estimated monthly cost based on return volume and average refund value
- Click Download Report button navigates to Report Page

**Specific Actionable Fixes by Category**:
- **Sizing issues**:
  - Add a size comparison chart showing brand-specific sizing vs standard sizing
  - Display measurements in both cm and inches for all product dimensions
  - Include a fit guide with body measurements and recommended sizes
- **Quality issues**:
  - Update supplier QC checklist with specific quality checkpoints
  - Add durability claims with supporting evidence such as material specifications or testing results
  - Improve packaging to prevent damage during shipping
- **Expectation mismatch**: Provide category-specific recommendations
- **Shipping damage**: Provide category-specific recommendations
- **Wrong item**: Provide category-specific recommendations

#### 3.6 Report Page

**Page Purpose**: Provide a clean formatted summary for sharing with suppliers or team members.

**Page Elements**:
- Editable field for store name
- Date of analysis
- Total number of returns analysed
- Top 3 issues with their specific actionable fixes
- Estimated monthly savings if issues are resolved
- Clean formatted summary of analysis results
- Copy button
- Download PDF button

**Functionality**:
- Display editable field for store name at the top of the report
- Display date of analysis automatically based on when the analysis was completed
- Display total number of returns analysed from the input data
- Display the top 3 return categories ranked by percentage share, along with their specific actionable fixes
- Calculate and display estimated monthly savings based on the number of preventable returns and average refund value
- Display analysis results in a clean, professional format suitable for sharing with suppliers or team members
- Click Copy button copies the entire report text to clipboard
- Click Download PDF button exports the report as a PDF file or triggers browser print dialog for PDF generation

### 4. Business Rules and Logic

#### 4.1 Return Category Classification
- The system categorises return reasons into five predefined categories: sizing, quality, expectation mismatch, shipping damage, wrong item
- Each return reason is assigned to the most relevant category
- Percentage share is calculated based on the number of returns in each category divided by total returns

#### 4.2 Cost Estimation Logic
- If average refund value is provided, calculate estimated monthly cost as: (number of preventable returns) × (average refund value)
- Preventable returns are those in categories where actionable fixes can be implemented

#### 4.3 Savings Calculation Logic
- Estimated monthly savings is calculated based on the assumption that implementing the recommended fixes will prevent a portion of returns in the top 3 categories
- Savings = (number of returns in top 3 categories) × (average refund value)

#### 4.4 Severity Colour Coding
- Categories are colour-coded based on percentage share to indicate severity level
- Higher percentage indicates higher severity and requires more urgent attention

#### 4.5 Priority Fix Badge Logic
- The category with the highest percentage share is identified as the number one issue
- A red Priority Fix badge is displayed on this category in the donut chart and ranked list

#### 4.6 Actionable Recommendations Logic
- For sizing issues, provide specific fixes: size comparison chart, measurements in cm and inches, fit guide
- For quality issues, provide specific fixes: supplier QC checklist updates, durability claims with evidence, packaging improvements
- For other categories, provide relevant actionable recommendations

#### 4.7 Navigation Flow
- Landing Page → Input Page → Processing Page → Results Dashboard → Report Page
- Users can return to Input Page from Results Dashboard to analyse new data

### 5. Exceptions and Edge Cases

| Scenario | Handling |
|----------|----------|
| User submits empty text area and no file | Display error message: Please provide return reasons via text input or file upload |
| Uploaded file format is not CSV or TXT | Display error message: Please upload a CSV or TXT file |
| Uploaded file is empty or contains no valid data | Display error message: The uploaded file contains no valid return reasons |
| Average refund value is negative or non-numeric | Display error message: Please enter a valid positive number for average refund value |
| No return reasons can be categorised | Display message: Unable to categorise the provided return reasons. Please ensure the data contains clear return reason descriptions |
| Copy to clipboard fails | Display error message: Failed to copy report. Please try again or manually select and copy the text |
| PDF download fails | Display error message: Failed to generate PDF. Please try using your browser's print function instead |
| Multiple categories have equal highest percentage | Display Priority Fix badge on the first category in the predefined order: sizing, quality, expectation mismatch, shipping damage, wrong item |
| Store name field is left empty | Use default text: Store Name in the report |
| Average refund value not provided | Display estimated monthly savings as: Unable to calculate without average refund value |

### 6. Acceptance Criteria

1. Landing page displays headline, value proposition, and CTA button clearly
2. Input page accepts return reasons via text area and file upload
3. Input page validates that at least one input method contains data before submission
4. Processing page displays animated loading state during analysis
5. Results dashboard displays a donut chart showing the breakdown of all five return categories with percentage shares
6. Results dashboard displays a red Priority Fix badge on the category with the highest percentage share
7. Results dashboard displays all five return categories with percentage shares and colour-coded severity bars
8. Results dashboard shows root cause and 3 actionable fixes for each category
9. For sizing issues, actionable fixes include: size comparison chart, measurements in cm and inches, and fit guide
10. For quality issues, actionable fixes include: supplier QC checklist updates, durability claims with evidence, and packaging improvements
11. Results dashboard calculates and displays estimated monthly cost when average refund value is provided
12. Report page displays editable field for store name
13. Report page displays date of analysis
14. Report page displays total number of returns analysed
15. Report page displays top 3 issues with their specific actionable fixes
16. Report page displays estimated monthly savings if average refund value was provided
17. Report format is clean and professional, suitable for sharing with suppliers or team members
18. Copy button successfully copies report text to clipboard
19. Download PDF button generates downloadable PDF or triggers print dialog
20. Application works entirely in browser without requiring user login
21. Design uses clean, professional blue and white colour scheme throughout
22. All pages are responsive and functional on desktop browsers

### 7. Out of Scope for This Release

- User authentication and login system
- Saving analysis history or previous reports
- Comparing multiple analysis reports
- Integration with e-commerce platforms or APIs
- Real-time data synchronisation
- Multi-language support
- Advanced filtering or sorting options in results
- Customising return categories beyond the five predefined ones
- Exporting results in formats other than PDF
- Email sharing functionality
- Mobile app version
- Collaborative features or team access
