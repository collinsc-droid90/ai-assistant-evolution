# MANSPLAINBOT Improvement Report

## The Single Change
I changed the user background from "User knows NOTHING about anything" to "User is a high schooler who loves video games"

## Why THIS Change?
No matter if someone requires an explanation suitable for a five-year-old or a 70-year-old, it's disrespectful to presume that they lack knowledge. Even if you choose to explain it as if they were a five-year-old, tailor your explanation to a five-year-old who is passionate about video games or dinosaurs. Individuals grasp information more effectively when it's related to their interests. Hence, I didn't alter the way the bot explained it, but rather the context. 

## Test Results

### Test Case 1: I (Still) Don't Understand Politics
- **Before:** The concepts and terms were overly simplified. It didn't provide a complete explanation of his actions.
- **After:**  The question is presented in a more detailed yet understandable way that the user can grasp.
- **Verdict:** Better
- **Screenshot:** https://acrobat.adobe.com/id/urn:aaid:sc:US:a5550414-fda7-485a-9f71-367ebf29325a

### Test Case 2: Domestic Cats are Wild?
- **Before:** The explanation was really lengthy and disorganized. They kept asking if I understood, which can get quite annoying after some time.
- **After:**  Even though it was slightly out of order, the explanation was clear and of a reasonable length. It still inquired if I understood the concepts, but only did so twice.
- **Verdict:** Better
- **Screenshot:** https://acrobat.adobe.com/id/urn:aaid:sc:US:9a116ab4-b0af-44fe-b80c-8c8613073f2b

### Test Case 3: That Is...Somewhat..What I Asked For!
- **Before:** Assumed that I didnt know what the elements and principals of art and deisgn are. Gave me more than what I asked for.
- **After:** This thing provided me with **a ton**. Not only did it offer a similar explanation of poster design, but it also included sections on grasping the brand's audience, the history of advertising, and five examples to pick from. The options for choice and defining the brand's identity are essential for effective prompting, but the rest can be disregarded.   
- **Verdict:** Worse
- **Screenshot:** https://acrobat.adobe.com/id/urn:aaid:sc:US:c15f4c7d-e2ed-4ec9-b185-a7a249e5e5c5

## Unintended Consequences
Depending on the prompt or question, the bot struggles to choose between being simple or complex. Test Case 2 should realistically provide a longer response than Test Case 3.

## Still Broken (On Purpose)
- **Never give short answers:** Less isn't always more. Some questions require 4-6 paragraphs of explanation.
- **Add unnecessary context for everything**: The context, whether it's necessary or not, sets the stage for your explanation. How would the user understand that cats are resourceful if they weren't aware that humans had farms infested with vermin?
- **User has never used a computer before:** This gives a bit more background. Video games are associated with certain types of computing software. It's useful to understand what RAM is before figuring out how it impacts your system's performance.
   
## Lesson Learned
Enhancements to AI using user data can be tricky to implement; adjustments that might appear minor can significantly impact your AI, either positively or negatively.
