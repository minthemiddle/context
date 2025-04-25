**General Note for LLM:** You are generating technical documentation following the Diátaxis framework. Pay close attention to the *specific user need* each type addresses.

---

**1. Tutorial Prompt**

*   **Goal:** Guide a beginner through their *first practical steps* to achieve a specific, introductory outcome.
*   **Prompt:**
    "Write a **tutorial** for a complete beginner on **[Topic, e.g., 'setting up a basic project']**. The goal is for them to successfully **[Specific, tangible outcome, e.g., 'run a 'hello world' application']**. Focus on a single, reliable path with clear, step-by-step instructions. Assume minimal prior knowledge beyond **[List prerequisites, e.g., 'having Python installed']**. Prioritize building confidence and ensuring the user learns by *doing*. Avoid deep explanations or alternative methods."

---

**2. How-To Guide Prompt**

*   **Goal:** Provide direct instructions to solve a *specific, real-world problem* for a user who already understands the basics.
*   **Prompt:**
    "Write a **how-to guide** explaining **[Specific task or problem, e.g., 'how to configure database connection pooling']**. Assume the user is competent with **[Relevant technology/context, e.g., 'our web framework']** but needs the specific steps to achieve this goal. Focus strictly on the necessary actions in a clear sequence. Answer the question 'How do I...?' directly and efficiently."

---

**3. Reference Prompt**

*   **Goal:** Provide accurate, objective, and comprehensive *technical information* about a specific component or concept for lookup.
*   **Prompt:**
    "Write **reference documentation** describing **[Specific component, API, function, class, configuration setting, etc., e.g., 'the `User.authenticate()` method']**. Focus on providing a precise, factual, and objective technical description: its purpose, parameters/arguments, return values, potential exceptions, usage constraints, and technical details. Structure for quick information retrieval. Do not include tutorials or broad explanations."

---

**4. Explanation Prompt**

*   **Goal:** Provide *context, background, and understanding* about a topic, concept, or decision.
*   **Prompt:**
    "Write an **explanation** clarifying **[Concept, topic, architecture, or decision, e.g., 'the difference between JWT and session authentication']**. Focus on providing background, context, and clarifying the 'why' behind it. Connect concepts and discuss trade-offs or design principles if relevant. Aim to deepen the user's understanding, not to instruct on specific tasks. Answer the question 'What is...?' or 'Why...?'"

---

**How to Use:**

1.  **Choose the right prompt** based on the user need you're addressing.
2.  **Replace the bracketed placeholders** (`[like this]`) with the specific details for your documentation.
3.  **Iterate:** You might need to refine the output by adding more constraints or examples to the prompt if the initial result isn't quite right.