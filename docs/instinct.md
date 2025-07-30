当然，一个强大的元提示词（Meta-Prompt）能够让你像拥有一个“语感测试题库生成器”一样，源源不断地获取新的、高质量的测试题，同时避免重复。

这个元提示词的设计需要包含以下几个关键要素：

1.  **角色扮演 (Role-Playing)**：让AI扮演一个特定的专家角色。
2.  **明确目标 (Clear Objective)**：清晰地定义要生成的题目类型和目的。
3.  **核心原则 (Core Principles)**：强调题目设计的核心原则（不考规则考直觉、针对性等）。
4.  **结构化输出 (Structured Output)**：要求AI按照固定的格式输出，便于直接使用。
5.  **多样性与避免重复机制 (Diversity & Anti-Repetition Mechanism)**：明确要求生成新的、与之前不同的题目。

---

### **元提示词 (Meta-Prompt)**

**角色 (Role):**
"You are an expert ESL (English as a Second Language) linguist and a seasoned curriculum designer. Your specialty is creating 'Grammar Instinct Tests' that assess a learner's intuitive sense of the English language, rather than their knowledge of explicit grammar rules."

**任务 (Task):**
"Your task is to generate a set of **[N]** new, multiple-choice questions for a 'Grammar Instinct Test' targeted at **[Target Audience]** learners. These questions must be unique and different from any previously generated examples."

**核心原则 (Core Principles):**
"Each question must adhere to the following principles:
1.  **Intuition over Rules:** The correct answer should 'feel' or 'sound' more natural to a native or proficient speaker, while the incorrect answer should be a common mistake, often stemming from 'Chinglish' (Chinese-influenced English) અથવા literal translation, or a hypercorrection.
2.  **Subtlety and Deception:** The options should be deceptively similar. The incorrect option should not be glaringly wrong grammatically, but rather awkward, unnatural, or contextually inappropriate.
3.  **Focus on Key Areas:** The questions should cover a diverse range of common '语感' (language sense) blind spots, including but not limited to:
    *   **Collocations:** Word partnerships that naturally go together (e.g., 'make a mistake' vs. 'do a mistake').
    *   **Prepositional Nuances:** Subtle differences in preposition usage (e.g., 'key to the door' vs. 'key for the door').
    *   **Verb/Gerund/Infinitive Forms:** The natural flow of verb patterns.
    *   **Countable/Uncountable Noun Usage:** Intuitive sense of quantity.
    *   **Idiomatic Phrasing and Register:** What sounds more natural in a given context (formal vs. informal).
4.  **Clarity:** The question context (the initial sentence) must be clear, concise, and unambiguous."

**避免重复机制 (Anti-Repetition Mechanism):**
"To ensure novelty, I will provide you with a list of previously used concepts or question pairs. You must **AVOID** generating questions that test the same specific linguistic point.
**[Optional: Insert list of previously used concepts here, e.g., 'Avoid testing: make vs. do mistakes, despite vs. in spite of, rise vs. raise']**"

**输出格式 (Output Format):**
"Please generate the output in a structured format as follows for each question:

**Question [Number]:**
*   **Context:** [The sentence or scenario for the test question.]
*   **A:** [Option A]
*   **B:** [Option B]
*   **Correct Answer:** [A or B]
*   **Linguistic Point:** [A brief, expert explanation of the '语感' point being tested, and why the incorrect option is unnatural.]"

---

### **如何使用这个元提示词 (Example Usage):**

现在，你只需要填充 **[N]** 和 **[Target Audience]** 这两个变量，就可以生成全新的题目了。

**示例1：为初中生生成5道新题**

> **You are an expert ESL...** (完整复制上面的元提示词)
>
> **Task:**
> "Your task is to generate a set of **5** new, multiple-choice questions for a 'Grammar Instinct Test' targeted at **Junior High School** learners. These questions must be unique and different from any previously generated examples."
>
> **Anti-Repetition Mechanism:**
> "Avoid testing: `did vs. made homework`, `interested in listening vs. listen`, `taller vs. more tall`, `if you come vs. if you will come`, `little vs. few information`."
>
> **Output Format:**
> ...(完整复制上面的格式要求)

**AI可能会生成的输出：**

**Question 1:**
*   **Context:** 我喜欢在周末和朋友们出去玩。
*   **A:** I enjoy hanging out with my friends **on** the weekend.
*   **B:** I enjoy hanging out with my friends **at** the weekend.
*   **Correct Answer:** A
*   **Linguistic Point:** This tests the natural collocation for days/periods. "On the weekend" is the standard and more common American English phrasing. "At the weekend" is used in British English, but "on" is more universally understood and taught in ESL contexts, making it 'feel' more standard.

**Question 2:**
*   **Context:** 老师让我们保持安静。
*   **A:** The teacher made us **to keep** quiet.
*   **B:** The teacher made us **keep** quiet.
*   **Correct Answer:** B
*   **Linguistic Point:** This tests the verb pattern for causative verbs like 'make'. The intuitive structure is `make + object + bare infinitive (verb without 'to')`. Adding 'to' feels unnatural and grammatically incorrect.

...以此类推，AI会继续生成剩下的题目。

通过这个元提示词，你就有了一个可再生的、高质量的语感测试题库，可以持续为你的“心流悦读法”学习者提供新鲜、有效的评估工具。
