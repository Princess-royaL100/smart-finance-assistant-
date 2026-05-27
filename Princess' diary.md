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

### Entry 5 – DEBUGGING THE CODE 
**Artifact:** Screenshot showing integration of hands-on-ai chat with pandas analysis.

<img width="746" height="330" alt="Screenshot 2026-05-27 120149" src="https://github.com/user-attachments/assets/a59cf270-7a7d-430c-b6aa-98483edebb5e" />

**Context:** I wanted AI help me debug the code because the one I Gemini had given me was producing errors. 

**My Prompt:** "Write a complete, single-cell Python implementation for Google Colab that handles the automatic installation of the 'hands-on-ai' package. Build a RAG text-retrieval context engine from a student budgeting guidelines markdown string, register a custom savings goal calculator function as an Agent Tool using the tool decorator, and seamlessly bind both with the 'Lifestyle Architect' chat persona in an aesthetic, tabbed Gradio interface featuring full diagnostic testing."

**Key Learning:** AI helped me come up with a code that was functional 

**Reflection:** Integrating multiple technologies requires understanding how each piece serves the business purpose. AI can generate technical integration code, but I need to guide it toward business value.

---

### Entry 6 – Professional Financial spending 
**Artifact:** Screenshot
<img width="861" height="495" alt="Screenshot 2026-05-27 122036" src="https://github.com/user-attachments/assets/b93129e4-22b8-4d72-a2dc-de70143a9add" />


**Context:** I need AI to help me execute a professional financial recommendations, spending analysis data and include specific savings opportunities spending.

**AI Suggestion:** To convert your processed transactional KPIs into high-impact, personal financial advice, you need an automated logical layer that interprets the data and structures it for your user interface.

Below is the complete Python implementation for the AI Insight Generator Component. It reads the output from your data pipeline, dynamically flags budget issues like "Lifestyle Leakage," and builds a structured, reader-friendly layout using Markdown.

import pandas as pd
from typing import Dict, Any

def generate_financial_recommendations(financial_kpis: Dict[str, Any]) -> str:
    """
    Analyzes calculated data summaries to construct dynamic, highly 
    tailored financial insights and savings opportunities for the user.
    """
    # 1. Extract foundational parameters from our calculated KPIs
    outflows = financial_kpis.get('net_outflows', 0.0)
    inflows = financial_kpis.get('net_inflows', 0.0)
    essential = financial_kpis.get('essential_allocation', 0.0)
    discretionary = financial_kpis.get('discretionary_allocation', 0.0)
    summary_df = financial_kpis.get('summary_dataframe', pd.DataFrame())
    ### Entry 7- 
    <img width="1287" height="612" alt="Screenshot 2026-05-27 152708" src="https://github.com/user-attachments/assets/3e3ffc34-07c7-46ff-aeed-9d5243fb29ee" />
When I am trying to Ask the chatbot some questions the application is outputting an error message. 


    
    # Calculate key benchmark percentages
    discretionary_pct = (discretionary / outflows * 100) if outflows > 0 else 0.0
    net_savings_margin = inflows - outflows
    
    # 2. Begin structuring our professional application advice panel
    markdown_report = "## 🏛️ Lifestyle Architect • Strategic Advisory Panel\n"
    markdown_report += "---\n\n"
    
    # =====================================================================
    # SECTION A: SPENDING PATTERN OBSERVATIONS
    # =====================================================================
    markdown_report += "### 📊 Spending Pattern Observations\n"
    
    if outflows == 0:
        markdown_report += "• ℹ️ **No Outflow Data Detected:** Upload an active transaction statement ledger to identify tracking trends.\n\n"
    else:
        markdown_report += f"• 🔍 **Capital Distribution Profile:** Your wallet allocation is currently split between **{100 - discretionary_pct:.1f}% Fixed Essentials** and **{discretionary_pct:.1f}% Flexible Discretionary** expenditures.\n"
        
        # Look for the single highest spending category in the dataframe matrix
        if not summary_df.empty:
            highest_row = summary_df.loc[summary_df['Total Expended'].idxmax()]
            markdown_report += f"• 📈 **Concentration Alert:** Your primary capital exposure is centered in the **{highest_row['Category']}** category, commanding a **{highest_row['Wallet Share %']}%** total share of your outlays.\n\n"

    # =====================================================================
    # SECTION B: TARGET ALIGNMENT & SYSTEM RISK LEVEL
    # =====================================================================
    markdown_report += "### 🛡️ System Risk Assessment\n"
    
    # Apply your official financial guideline rules explicitly via conditional checks
    if discretionary_pct > 50.0:
        markdown_report += (
            "> 🚨 **CRITICAL RISK: Lifestyle Leakage Crisis Triggered!**\n"
            f"> Your flexible variable spending (**{discretionary_pct:.1f}%**) crosses the healthy 50.0% structural "
            "baseline. This profile drains your liquid capital margin. Non-essential leisure transactions should be capped immediately.\n\n"
        )
    elif discretionary_pct > 30.0:
        markdown_report += (
            "> ⚠️ **MODERATE WARNING: Elevated Flexible Outlays**\n"
            f"> Variable choices are consuming **{discretionary_pct:.1f}%** of your wallet share. While not in a deep crisis, "
            "trimming non-essential commercial vendor purchases will rapidly boost your safety savings trajectory.\n\n"
        )
    else:
        markdown_report += (
            "> ✅ **OPTIMAL ALLOCATION: Stable Structural Balance**\n"
            f"> Excellent financial architecture! Your flexible choices are safely limited to **{discretionary_pct:.1f}%**, "
            "keeping your capital securely insulated under baseline limits.\n\n"
        )

    # =====================================================================
    # SECTION C: ACTIONABLE SAVINGS OPPORTUNITIES
    # =====================================================================
    markdown_report += "### 💡 Actionable Advice & Savings Opportunities\n"
    
    if net_savings_margin <= 0:
        markdown_report += (
            "1. 🛑 **Deficit Mitigation:** Your monthly burn rate exceeds your income inflows by **${abs(net_savings_margin):,.2f}**. "
            "Prioritize meal-prepping over food delivery apps and cancel unused digital entertainment subscriptions immediately to plug the gap.\n"
        )
    else:
        markdown_report += (
            f"1. 📥 **Automated Wealth Sweep:** You have a positive liquid surplus of **${net_savings_margin:,.2f}**. "
            "Configure an automatic bank transfer rule to sweep 20% of incoming deposits directly into a high-yield capital savings account.\n"
        )
        
    markdown_report += (
        "2. 🪪 **Campus Resource Optimization:** Leverage your university student profile to capture Guild cafe concessions, "
        "discounted software developer tools, and off-peak public transit concessions to secure easier margins.\n"
    )
    markdown_report += (
        "3. 🛒 **Variable Substitution Strategy:** Substitute restaurant dinners with organized group cooking. This simple pivot "
        "recovers an average of $45 weekly from discretionary leakage arrays.\n"
    )
    
    return markdown_report

# =====================================================================
# 🧪 STEP 6 METHODOLOGY: AUTOMATED ADVICE INTEGRITY TEST
# =====================================================================
print("🧪 Running Strategic Insight Logic Verification Check...")
print("=" * 70)

# Simulate passing our calculated variables from the previous step 
# (Total Outflow: $696.50, Essential: $579.50, Discretionary: $117.00 -> ~16.8% Discretionary Share)
test_kpis = {
    'net_outflows': 696.50,
    'net_inflows': 1200.00,
    'essential_allocation': 579.50,
    'discretionary_allocation': 117.00,
    'summary_dataframe': pd.DataFrame([
        {'Category': 'Rent', 'Total Expended': 450.00, 'Wallet Share %': 64.6},
        {'Category': 'Entertainment', 'Total Expended': 120.00, 'Wallet Share %': 17.2}
    ])
}

# Generate the advice content payload
app_insights_panel = generate_financial_recommendations(test_kpis)

# Assert Check: Ensure the calculation logic accurately matches our structural rules
assert "Stable Structural Balance" in app_insights_panel, \
    "Axiom Failure: Advice controller picked the wrong category risk marker."
print("Encoding Test: Verified. System correctly calculated low discretionary exposure and flagged it as 'Stable'.")
print("-" * 70)

# Print out the clean, rendered Markdown result
print(app_insights_panel)
```

---
### Entry 5 – DEBUGGING THE CODE 

