# Activity: Refactor "Check It!" into Components

## Setup
- Meet up in groups of 3.
- Clone and/or fork the provided repo. It contains all the starter code and a copy of the instructions in the readme. (remember to install the dependencies)
- While everyone will work in their own repo version, you'll plan out how to refactor the code together. The goal here is for the refactoring to be intentional. You'll likely deviate from your original plan - this needs to be discussed, try to anticipate problems and benefits from your decisions.
- As you work through this, follow the workflow: Evaluate -&gt; Plan -&gt; Do -&gt; Test. Consider your assumptions and questions as you progress
The situation

**App.js works, but it's a wall of JSX — everything from the header to the footer lives in one function. That's the code smell you're fixing today.**

## Your task
- Refactor the screen so the same UI renders from clearly separated, reusable components, connected only through props (one-way data flow). Nothing should look or behave differently when you're done — you're reorganizing, not redesigning.
- Step through the code and identify what it is doing, make sure you understand all the different parts before you plan to chop it up
- Using paper, figjam or any whiteboarding software (or a real whiteboard), decide what code should go into what components. Consider the input and output of each component.
- Create a components/ folder in your repo and decide who will start with which component, try to divide the tasks up so everyone is starting at a different piece (ie: 1 person might start by creating the new pressable buttons while someone else is working on the page layout content while another works on the list rendering)
- As you build, regularly test your work to make sure it's going together. Collaborate and feel free to share code + ideas of how to organize.

**App.js should end up short: mostly imports and a handful of components stacked inside the SafeAreaView/ScrollView.**

## Requirements
-Each component lives in its own file under components/.
- Data flows down via props only. No component should hard-code data that its parent already has (e.g. a TodoItem component shouldn't know about the full&nbsp;todoItems array, only the one item it was given).
- Determine which components should always have the same information and not use props (or if you want all of them to use props)
- Keep the map method that renders the list in place for now.
- Styles should move with their component (each file keeps its own StyleSheet.create), or live in a shared styles/colors.js for the Catppuccin palette — your call, but be consistent.
- The two CTA buttons and the two task buttons still just console.log for now no real logic yet.
- Buttons are replaced with Pressable that are custom styled to introduce visual hierarchy

## Self-check
-[ ] App.js no longer contains any raw <text>/<view> markup for the header, description, input demo, todo cards, or footer, those all come from imported components.
-[ ] The app still looks and behaves exactly like the starter version.
-[ ] Every prop your components receive is actually used — no dead props.
-[ ] TodoItem is generic enough that it doesn't reference todoItems by name anywhere.
-[ ] The list refactoring comments are still there

## Reflection Questions (answer at least 3)

- What were relevant criteria for you to determine if something should be it's own component?
- When in your workflow should you do a refactor like this? (ie: we still don't have functioning logic, would you have preferred to wait until that was completed? or does doing it after the content is visually built out make more sense)
- Did you and your teammates disagree on how to approach any components? consider the positions behind the different approaches
- What was your biggest takeaway from this activity?
- What is unclear after doing this activity?
