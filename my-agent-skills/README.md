# 🤖 My Agent Skills Library

A collection of AI agent skill prompts (SKILL.md files) for n8n multi-agent systems.

> **Remember:** A "Skill" = a sub-workflow with a focused system prompt 😄

## 📁 Structure

```
my-agent-skills/
├── master/
│   └── orchestrator.md          # Master routing agent
├── skills/
│   ├── marketing/
│   │   ├── ads-copy-generator.md
│   │   ├── marketing-research.md
│   │   └── wiki-llm-generator.md
│   ├── social-media/
│   │   ├── social-media-post-writer.md
│   │   ├── content-calendar-planner.md
│   │   └── hashtag-researcher.md
│   ├── automation/
│   │   ├── n8n-workflow-builder.md
│   │   └── automation-architect.md
│   ├── ai-automation/
│   │   ├── ai-agent-architect.md
│   │   └── prompt-engineer.md
│   └── rag/
│       ├── rag-pipeline-builder.md
│       └── knowledge-base-curator.md
```

## 🚀 How to Use in n8n

Fetch any skill prompt via HTTP Request:
```
https://raw.githubusercontent.com/YOUR_USERNAME/my-agent-skills/main/skills/marketing/ads-copy-generator.md
```

## 📊 Skills Index

| Skill | Category | Description |
|---|---|---|
| Master Orchestrator | Core | Routes to right skill |
| Ads Copy Generator | Marketing | Meta, Google, TikTok ad copy |
| Marketing Research | Marketing | Competitor & audience research |
| Wiki LLM Generator | Content | Structured docs & knowledge base |
| Social Media Writer | Social | Posts for all platforms |
| Content Calendar | Social | Monthly content planning |
| Hashtag Researcher | Social | Hashtag strategy |
| n8n Workflow Builder | Automation | n8n help & debugging |
| Automation Architect | Automation | Business process automation |
| AI Agent Architect | AI | Multi-agent system design |
| Prompt Engineer | AI | Prompt writing & optimization |
| RAG Pipeline Builder | RAG | Vector stores & doc Q&A |
| Knowledge Base Curator | RAG | KB organization & FAQs |

## 🔗 Load Skill in n8n

Add HTTP Request node BEFORE your AI Agent node:
- Method: GET
- URL: raw GitHub URL of the skill
- Response: Text
- Use: `{{ $json.data }}` as system message

Built with ❤️ from Alexandria, Egypt 🇪🇬
