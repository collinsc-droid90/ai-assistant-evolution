# 💡 The Inspirer: MVP Product Requirements Document (PRD)

### 1. 🎯 Product Goal
The goal of The Inspirer MVP is to provide graphic designers with immediate, structured creative prompts to overcome creative blocks and accelerate the initial ideation phase of a project.

### 2. 📝 Problem Statement
Graphic designers frequently experience creative block or feel intense pressure to generate fresh, innovative concepts quickly for client projects or personal work. Existing resources often offer generic inspiration, requiring significant time and effort to translate into actionable design concepts.

### 3. 👤 Target User
-	Primary User: Graphic Designers (Student to Mid-Level)
-	Demographics: Ages 18-35, comfortable with digital tools.
-	Goal: To quickly find a starting point or a unique angle for a design project (e.g., logo, poster, web element) when they feel stuck.
-	Pain Point: The blank canvas; the mental fatigue of forced ideation; time constraints.

### 4. ✨ Must-Have MVP Features
These three features are essential to solve the core problem for the target user in the first version.

| Feature Name | Description | Rational |
|:-----|:---:|-----:|
| Concept Mixer (Core Feature) | Generates a prompt by randomly combining three distinct elements: a Design Style (e.g., Brutalism, Art Deco, Minimalist), a Target Audience (e.g., Gen Z, Senior Citizens, Tech Startups), and an Emotion/Concept (e.g., Nostalgia, Anxiety, Transparency).  | Directly addresses creative block by forcing unconventional combinations, providing a concrete starting point. |
| Project Type Filter | Allows the user to select the type of project before generating the prompt (e.g., Logo Design, Social Media Ad, Web UI Element, Packaging). | Ensures the generated prompt is relevant and actionable for the designer's current task, increasing immediate utility. |
| Prompt History & Save | A simple list view that records the last 5-10 generated prompts and allows the user to save a prompt to a separate "Favorites" list for later use. | Prevents loss of good ideas and lets the user quickly revisit and compare options without having to re-generate them. |

### 5. 🔁 User Interaction Flow (Concept Mixer)
This flow outlines the user journey for the core functionality.

**1.	Start:** User lands on the main screen.

**2.	Select Project Type:** User selects a Project Type Filter (e.g., "Logo Design").

**3.	Generate Prompt:** User clicks a prominent "Inspire Me!" button.

**4.	Display Result:** The application generates and displays the unique three-part concept prompt (e.g., Style + Audience + Emotion).

-----

### 🗄️ Concept Mixer Data Structure
The core of the Concept Mixer relies on three independent arrays (or lists) that the application will randomly select one item from each to construct the final prompt.
1. 🎨 Design Styles (Minimum of 10)
This list defines the aesthetic direction or movement for the project.

| Variable Name | DESIGN_STYLES |  |
|:-----|:---:|-----:|
| Data Type | Array of Strings |  
| Example Items | 1. Minimalism |
|  | 2. Brutalism |
|  | 3. Art Deco |
|  | 4. Swiss/International Style |
|  | 5. Psychedelic |
|  | 6.Vaporwave |
|  | 7. Hand-Drawn/Illustrative |
|  | 8. Glitch/Digital Distortion |
|  | 9. Memphis Style |
|  | 10. Neumorphism|

2. 👤 Target Audiences (Minimum of 10)
This list defines the specific group of people the design must appeal to, forcing the designer to consider context and usability.

| Variable Name | TARGET_AUDIENCES |  |
|:-----|:---:|-----:|
| Data Type | Array of Strings |  
| Example Items | 1. Gen Z / Teens |
|  | 	2. Senior Citizens (65+) |
|  | 	3. Tech Startup Employees |
|  | 	4. High-End Luxury Consumers |
|  | 	5. Local Community Members |
|  | 6. Parents with Young Children |
|  | 7. Financial/Investment Professionals |
|  | 8. Eco-Conscious Consumers |
|  | 9. Small Business Owners |
|  | 10. Gaming Enthusiasts|

3. 🧠 Emotions / Concepts (Minimum of 10)
This list defines the feeling, abstract idea, or core message the design must convey or revolve around.

| Variable Name | EMOTIONS_CONCEPTS |  |
|:-----|:---:|-----:|
| Data Type | Array of Strings |  
| Example Items | 1. Nostalgia |
|  | 	2. Anxiety/Urgency |
|  | 	3. Transparency/Openness |
|  | 	4. Optimism/Hope |
|  | 	5. Isolation/Solitude |
|  | 6. Transformation/Change |
|  | 7. Power/Authority |
|  | 8. Playfulness/Whimsy |
|  | 9. Mystery/Intrigue |
|  | 9. Sustainability/Natural Growth |

4. 📝 Project Type Filter Data
You will also need a separate list for the Project Type Filter feature (Section 4 of the PRD).

| Variable Name | PROJECT_TYPES |  |
|:-----|:---:|-----:|
| Data Type | Array of Strings |  
| Example Items | 1. Logo Design |
|  | 	2. Poster/Print Ad |
|  | 	3. Mobile App UI Screen |
|  | 	4. HSocial Media Campaign |
|  | 	5. Book Cover Design |
|  | 6. Packaging Design |

### Generated Prompt Structure

When the user clicks "Inspire Me!", the output should follow this format:

**Project:** [Random Item from PROJECT_TYPES]

**Design Prompt:** Create a design in the [Random Item from DESIGN_STYLES] style, targeting [Random Item from TARGET_AUDIENCES], and conveying the feeling of [Random Item from EMOTIONS_CONCEPTS].

*Example Output:*

**Project:** Logo Design

**Design Prompt:** Create a design in the Brutalism style, targeting Eco-Conscious Consumers, and conveying the feeling of Transformation / Change.

-----

**5.	Review Options:** User views the prompt. They have two immediate actions:

-	Action A (Discard/Rethink): User clicks the "Inspire Me!" button again. The new prompt is generated, and the previous one is moved to Prompt History.

-	Action B (Keep): User clicks the "Save to Favorites" button. The prompt is moved to the Favorites list.

**6.	Exit:** User closes the app or navigates to the History/Favorites section to review saved ideas.

### 6. 🚫 Exclusions from V1
To keep the MVP focused and launchable quickly, the following features will be excluded from the initial release:

•	Image Generation/AI Mockups: No integration with external APIs for generating visual examples based on the prompt. The focus is purely on textual ideation.

•	User Accounts & Cloud Sync: No need for login, registration, or syncing data across devices. Prompt History and Favorites will be stored locally (e.g., using local storage).

•	Collaboration Features: No sharing, commenting, or team functionality. This is a single-user tool.

•	Advanced Prompt Customization: No ability for the user to 'lock' one of the three variables (Style, Audience, or Emotion) while regenerating the others. All three must be random in V1.
