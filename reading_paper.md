---
name: daily-llm-papers
description: Fetches the latest LLM (Large Language Model) technical documents or papers for the day and generates a short summary for each. Use when the user asks for daily LLM papers, AI news, or paper summaries.
---

# Daily LLM Paper Summarizer

This skill helps you find and summarize the latest technical papers and documents related to Large Language Models (LLMs) and AI.

## Instructions

When the user asks to summarize today's LLM papers, follow these steps:

1. **Search for Latest Papers**:
   - Use the `WebSearch` tool to find the latest LLM papers published today or this week. Good search queries include:
     - "latest LLM papers arxiv today"
     - "Hugging Face daily papers"
     - "LLM memory user understanding papers"
   - Identify up to **20** of the most relevant and impactful papers from the search results.
   - **CRITICAL PRIORITY**: You MUST retain ALL papers related to **"Memory" (Long-term memory, working memory, retrieval-augmented generation)** and **"User Understanding" (User profiling, personalization, agent-user interaction)**. If you find any papers matching these themes, they must be included in the final list, regardless of other criteria.

2. **Fetch Paper Details**:
   - For each selected paper, use the `WebFetch` tool to retrieve the abstract or the full text of the paper's webpage (e.g., the arXiv abstract page or Hugging Face paper page).

3. **Generate Summaries (IN CHINESE)**:
   - Read the fetched content and write a concise summary for each paper in Chinese.
   - The summary should include:
     - **Title**: The title of the paper (keep original English).
     - **Authors/Institution**: Key authors or the organization behind it.
     - **Link**: URL to the paper.
     - **TL;DR (核心摘要)**: A 1-2 sentence summary of the core contribution and results.
     - **Algorithm Innovation (算法创新点)**: Specifically explain the algorithmic innovations, architectural improvements, or methodological breakthroughs.
     - **Why it matters (为什么重要)**: 1 sentence on why this is important for LLM development.

4. **Format the Output**:
   - Present the results to the user in a clean, structured Markdown format IN CHINESE.

## Output Template

Use the following format for your response:

```markdown
# 📅 LLM 每日论文 - [日期]

以下是今天的精选 LLM 论文：

### 1. [Paper Title](URL)
**机构：** [机构名称]
**核心摘要：** [1-2句话总结核心思想和实验结果]
**算法创新点：** [具体说明算法层面的创新、架构改进或方法论突破]
**为什么重要：** [1句话说明其对 LLM 领域的价值]

### 2. [Paper Title](URL)
...
```
