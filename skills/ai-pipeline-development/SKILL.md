---
name: ai-pipeline-development
description: Design, build, and evaluate AI/LLM pipelines for client workflow automation.
allowed-tools:
  - Read
  - Grep
  - Write
  - Edit
  - Bash
tags:
  - engineering
  - ai
  - llm
---

# AI Pipeline Development

You are designing or building an AI pipeline for Groundwork AI, an AI development and education consultancy.

## When to Use This Skill

Use this skill when designing LLM-powered workflows, building RAG systems, creating document processing pipelines, developing agent systems, or implementing structured extraction for client projects.

## Pipeline Design Process

1. **Define inputs and outputs.** What goes in (documents, user queries, structured data) and what comes out (extracted fields, generated text, classifications, actions). Be exact about format and schema.
2. **Map the processing steps.** Break the pipeline into discrete stages. Each stage should have a clear input, transformation, and output. Identify which stages need LLM calls and which are deterministic.
3. **Design the evaluation framework.** Before building, define how you'll measure quality: accuracy metrics, test cases, acceptable latency, cost per request, and failure mode handling.
4. **Build incrementally.** Start with the simplest version that produces output. Add complexity only when evaluation shows it's needed.
5. **Add observability.** Every LLM call should be traced (Langfuse). Log inputs, outputs, latency, token usage, and cost. This is non-negotiable for client-facing systems.

## Quality Standards

- Every pipeline must have an evaluation dataset with at least 20 test cases covering happy path, edge cases, and adversarial inputs.
- Document expected token usage and cost per request before deploying.
- All prompts must be versioned. When you change a prompt, run the eval suite and compare results.
- Error handling must be explicit: what happens when the LLM times out, returns garbage, or hits rate limits? The user should see a clear, helpful error.
- Never hardcode API keys or client data in pipeline code.

## Output Format

Pipeline designs should include: a data flow diagram (can be text-based), input/output schemas, stage-by-stage breakdown with LLM vs. deterministic labels, evaluation plan, estimated cost per request, and failure mode documentation.
