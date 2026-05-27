<img width="806" height="229" alt="Screenshot 2026-05-27 115228" src="https://github.com/user-attachments/assets/a84c0347-bd14-4e24-976f-5f13ee1a16db" /># 📓 Developer's Diary – AI Collaboration Guide

This file shows sample entries for your **Developer's Diary**. You must document your AI collaboration throughout the project development. Each entry should have:
- **Artifact**: a screenshot, GIF, or snippet of your AI interaction
- **Context**: one-sentence description of your goal
- **Reflection**: analysis of what happened, what you learned, and how you improved the solution

**Key Principle**: You're directing AI like a junior developer - always review, critique, and improve their suggestions.



## Foundation Skills Examples

### Entry 1 – Effective AI Prompting for Business Data
**Artifact:** Screenshot of ChatGPT conversation about analyzing spending data.

<img width="887" height="393" alt="Screenshot 2026-05-27 111313" src="https://github.com/user-attachments/assets/7f8d8799-84f1-4518-8628-b4d7633718a6" />


**My Initial Prompt:** "Help me analyze CSV data with pandas"

**My Improved Prompt:** Create a function to load a personal finance CSV transaction data with Date, Amount, Category, and Description columns. Handle Australian dollar signs, commas, and negative signs in the Amount column. If Category or Description are missing, fill them with 'Uncategorized'. Include clear, user-friendly error messages."

**Context:** Learning to write specific, business-focused AI prompts.


### Entry 2 – Critiquing and Improving AI Code
**Artifact:** Before/after screenshots of AI-generated spending analysis code. 

<img width="911" height="345" alt="Screenshot 2026-05-27 113301" src="https://github.com/user-attachments/assets/c4ef54cf-eb6a-4fdf-8d2e-4d5f957b69b4" />

**Context:** AI gave me a code that had errors, I then asked AI to help me dubug the code.

**AI's First Response:**
To resolve the connection error in Google Colab, we need to explicitly assign your system personality prompt using the hands_on_ai framework's proper syntax before calling for responses.

The main issue causing a connection failure or model confusion in the previous snippet is that passing a long instructions paragraph directly inside get_response() without setting up a chat history or a system role prompt can make the LLM server reject the query or return an empty error response.

Here is the fully debugged, production-ready implementation combined into a single cell. This uses the hands_on_ai.chat module's proper state configuration to ensure the AI knows its role perfectly.

**Reflection:** I learnt that sometimes AI might make mistakes and the code that the AI can give you may need debugging for it to work perfectly. 
---

### Entry 3 – Business Context in AI Interactions
**Artifact:** Screenshot of Gemini generating financial insights from data.

<img width="798" height="242" alt="Screenshot 2026-05-27 111945" src="https://github.com/user-attachments/assets/00595ff5-c3c2-46bb-b3b1-9c3c16289f99" />

**Context:** I want AI to create a code that will allow the user to input their CSV File.  

**My Prompt:** "Create a function to load a personal finance CSV transaction data with Date, Amount, Category, and Description columns. Handle Australian dollar signs, commas, and negative signs in the Amount column. If Category or Description are missing, fill them with 'Uncategorized'. Include clear, user-friendly error messages."

**AI Response:** 
This code opens your CSV file, strips out messy dollar signs, ensures all numbers are readable by Python, and catches missing categories.

**Reflection:** When I include business context and specify the audience (personal finance app users), AI generates much more relevant and professional output. I learned that framing requests in business terms gets business-quality responses. Now I always think about who will read the output and what decisions they need to make.

---

### Entry 4 – Intergration 

**Artifact:** Screenshot of debugging session with Claude about handling messy CSV data.
<img width="806" height="229" alt="Screenshot 2026-05-27 115228" src="https://github.com/user-attachments/assets/701e2ae0-de7f-4849-b997-7dde60a1b267" />

**Context:** My application should be able to chat with the user, retrive from CSV or other documents, it should have a Agent Tool and Gradio UI. 

**My Prompt:** "Create a Python script using the hands-on-ai library to authenticate with an Ollama server at 'https://ollama.serveur.au' running 'llama3.2'. Use a secure environment variable setup for the API key 'isys2001-assignment-key'. Include a robust try-except connection test to verify that the chatbot can successfully greet the user as 'The Lifestyle Architect'." 

**AI Solution:** This is where we transition into the advanced AI integration. We are going to implement the Hands-on-AI Configuration exactly as required by your lecturer's template, but tailored beautifully to fit "The Lifestyle Architect" system. 
# Handle refunds and missing data appropriately
df_clean = df.dropna(subset=['Amount_Clean'])
positive_spending = df_clean[df_clean['Amount_Clean'] > 0]
refunds = df_clean[df_clean['Amount_Clean'] < 0]
```


**Reflection:** Automation Over Manual Input: Instead of forcing your user (or your marker) to use a slow getpass() prompt to manually type in the key every single time they hit "Run Cell", this hardcodes the semester key isys2001-assignment-key safely into the environment instantly.

Contextual Testing: Instead of sending a generic "Hello", it passes a fast system message instructing the backend AI to act like The Lifestyle Architect. This acts as a preview for your marker that your theme is active.

## Advanced Integration Examples

### Entry 5 – DEBUGGING THE CODE 
**Artifact:** Screenshot showing integration of hands-on-ai chat with pandas analysis.

<img width="746" height="330" alt="Screenshot 2026-05-27 120149" src="https://github.com/user-attachments/assets/a59cf270-7a7d-430c-b6aa-98483edebb5e" />

**Context:** I wanted AI help me debug the code because the one I Gemini had given me was producing errors. 

**My Approach:** Used AI to help me combine CSV analysis with hands-on-ai chat functionality.

**Key Learning:** AI helped me structure the integration, but I had to understand the business logic to make it useful. The chatbot needed to understand financial concepts, not just execute code.

**Reflection:** Integrating multiple technologies requires understanding how each piece serves the business purpose. AI can generate technical integration code, but I need to guide it toward business value.

---

### Entry 6 – Professional Error Handling
**Artifact:** Code snippet showing error handling for file uploads.

**Context:** I needed my Gradio interface to handle bad CSV files gracefully.

**AI Suggestion:** Generated try/catch blocks with business-appropriate error messages:
```python
try:
    df = pd.read_csv(file.name)
    # Analysis code...
except FileNotFoundError:
    return "Please upload a valid CSV file."
except pd.errors.EmptyDataError:
    return "The uploaded file appears to be empty. Please check your data."
```

**Reflection:** AI helped me think about user experience, not just technical functionality. Good error messages help users understand what went wrong and how to fix it. This is crucial for business applications.

---

## AI Collaboration Best Practices I've Learned

### 🎯 Effective Prompting Strategies
1. **Always provide business context**: "I'm building a finance assistant for..."
2. **Specify data structure**: "My CSV has columns X, Y, Z with these data types..."  
3. **Request professional formatting**: "Format output for business presentation"
4. **Ask for comments**: "Include clear comments explaining the business logic"

### 🤔 Critique Questions I Always Ask
- "Does this handle edge cases like negative amounts or missing data?"
- "Are the variable names clear for a business context?"
- "How would I explain this code to a non-technical manager?"
- "What assumptions is this code making about my data?"

### 🔄 Iterative Improvement Process
1. **Get basic working code** from AI
2. **Test with real data** and find issues  
3. **Ask AI to fix specific problems** with context
4. **Simplify complex solutions** for maintainability
5. **Add business-appropriate formatting** and error handling

### 📊 Business Value Focus
- Always connect code back to business decisions
- Format outputs for non-technical users
- Include actionable insights, not just data summaries
- Consider the end user's needs and context

---

## 📝 Documentation Template for Your Entries

Use this format for consistent diary entries:

```markdown
### Entry [Number] – [Descriptive Title]
**Artifact:** [Screenshot/code snippet/GIF of AI interaction]

**Context:** [One sentence: what you were trying to achieve]

**My Prompt:** "[Your exact prompt to AI]"

**AI Response Summary:** [Brief description of what AI provided]

**My Critique/Improvement:** [How you modified or improved the AI's suggestion]

**Result:** [What you ended up with and why it's better]

**Reflection:** [What you learned about AI collaboration, business programming, or problem-solving]
```

---

✅ **Remember**: Document your AI collaboration throughout your project development. Each entry should show learning and improvement, not just successful interactions. Show how you direct AI like a junior developer to create business-appropriate solutions.

