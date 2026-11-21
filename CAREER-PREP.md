# Career Prep & Skill Gap Log

## 1. Industry Skill Research
> **Search Query:** "Find the top 5 most in-demand entry-level full-stack web development skills in India in 2026."

- **Top 5 In-Demand Skills:**
  1. **React.js & Next.js:** Building interactive Single Page Applications (SPAs) and Server-Side Rendered (SSR) web apps.
  2. **TypeScript:** Adding static type safety to catch runtime bugs early in production codebases.
  3. **Node.js & RESTful APIs:** Creating scalable backend services and connecting frontends to databases.
  4. **PostgreSQL & Databases:** Managing structured relational data, authentication, and queries.
  5. **Git & GitHub:** Version control, pull requests, and collaborative team workflows.

---

## 2. Market Verification (8 Entry-Level Job Postings on LinkedIn)
| Skill | Frequency (out of 8) | Source Verified? | Current Status |
| :--- | :---: | :---: | :---: |
| JavaScript | 8 / 8 | Yes | Proficient |
| React.js | 7 / 8 | Yes | Proficient |
| Git & GitHub | 7 / 8 | Yes | Proficient |
| Node.js / REST APIs | 6 / 8 | Yes | Proficient |
| TypeScript | 5 / 8 | Yes | Target Skill Gap |

---

## 3. Target Skill Gap
- **Focus Area:** Building and typing full-stack React components and API integrations using strict **TypeScript** without compiler errors.

---

## 4. 7-Day Study Plan (TypeScript for React)
- **Day 1: TypeScript basics (outside React)**

Learn: primitive types, arrays, type vs interface, union types ("a" | "b"), optional properties (?), function parameter and return types.
Task: In day1.ts, define type Student = { id: number; name: string; year?: 1 | 2 | 3 | 4 }. Write getLabel(s: Student): string and average(nums: number[]): number. Add 3 sample students in an array.
Check: npx tsc --noEmit passes. Deliberately pass a wrong type, confirm you get an error, then fix it.

- **Day 2: Typing props**

Learn: typing component props, optional props, default values, children: React.ReactNode, union props for variants.
Task: Build <Button label variant="primary" | "danger" onClick? /> and <Card title>{children}</Card>. Render 3 buttons and 2 cards in App.tsx.
Check: zero errors, and variant="blue" gives a compile error.

- **Day 3: Typing state with useState**

Learn: inferred vs explicit state types, useState<string | null>(null), arrays and object state, immutable updates.
Task: Build a Todo list: type Todo = { id: number; text: string; done: boolean }. Support add, toggle, and delete.
Check: zero errors, and all three actions work in the browser.

- **Day 4: Typing events and forms**

Learn: React.ChangeEvent<HTMLInputElement>, React.FormEvent<HTMLFormElement>, React.MouseEvent, controlled inputs, useRef<HTMLInputElement>(null).
Task: Build a signup form (name, email, year dropdown) with a typed form-state object, a single handleChange for all fields, and validation messages.
Check: zero errors. Submitting logs a correctly typed object.

- **Day 5: Typing API data with useEffect**

Learn: typing fetch responses, loading/error/data states, useEffect cleanup, generics (Promise<User[]>), unknown vs any.
Task: Fetch https://jsonplaceholder.typicode.com/users, define a User type, and render a list with loading and error states plus a search box that filters it.
Check: zero errors, and the list, loading state, and error state (test by breaking the URL) all work.

- **Day 6: Custom hooks, Context, and useReducer**

Learn: typing a custom hook's return value, createContext<T | null>(null), typed reducer actions as a discriminated union.
Task: Build a useCounter hook, then a ThemeContext (light/dark) with a typed provider and a useTheme() hook that throws if used outside the provider.
Check: zero errors, and the toggle updates two separate components.

- **Day 7: Test day (90 minutes, no AI, no copy-paste from old code)**

---  Build a "Task Tracker" mini-app from a blank folder:

------ A Task type: id, title, priority: "low" | "medium" | "high", done
------ A typed TaskForm component with props (onAdd) and a form with typed events
------ A TaskList component with typed props, toggle and delete
------ A filter by priority, using typed state
        Load 5 starter tasks from https://jsonplaceholder.typicode.com/todos?_limit=5, mapped into your Task type
        State shared via Context or lifted state*

---

## 5. Mock Technical Interview & Feedback
- **Question:** What are props and state in React, and when would you use each?[cite: 24]
- **My Answer:** Props are used to send data from one component to another and cannot be changed, while state is used to store data inside a                     component that changes when the user clicks something.
- 
- **Feedback & Score:**
-   **Score**: *6/10*. Your answer correctly identifies the core distinction—props are passed in and state changes within a component—but it is          too brief and contains a technical imprecision about props being “cannot be changed.”
-   **Two weakest points**
      “Props cannot be changed” is incomplete. Props are read-only within the child component; a parent can re-render the child with different         prop values. Saying they “cannot be changed” without that context can sound inaccurate. React treats props and state as immutable               snapshots and expects you to pass new props rather than mutate them.

State is not only for clicks. State can track any changing UI data—form input, loading status, API results, selected tabs, or modal visibility. Your answer narrows it to “when the user clicks something,” which understates its use. React recommends state for data expected to change over time, including user interaction.
---

## 6. Peer Review Observation
- "The explanation was clear and confident; reducing filler words like 'so' and 'like' will make technical answers sound even sharper."

---

## Weekly Goal
> **"The one skill I will improve this week is writing strict TypeScript for React components."**
