# DataOps-Gym  
## A Code-Driven SQL Environment for Enterprise Analytics Agents  

---

# 1️⃣ Core Idea (Simple + Achievable)

We build the **first reinforcement-learning style environment** where LLM agents interact with:

- A live SQL database  
- A real enterprise-like schema (multi-table relational)  
- A documentation corpus (business definitions, policies)  
- Executable query feedback  

And are evaluated on:

> Can the agent generate correct, definition-aware, evidence-grounded enterprise insights?

This is not a toy Text-to-SQL benchmark.

It is a **closed-loop, code-driven analytics environment**.

---

# 2️⃣ The Core Pain Point (Product-Driven)

The biggest blocker to AI Data Explorer adoption:

> “I don’t trust AI-generated analytics.”

Trust fails when:

- SQL joins are subtly wrong  
- Metric definitions are misapplied  
- Wrong segment filters are used  
- Numbers don’t reconcile  
- Reports are non-auditable  

DataOps-Gym directly evaluates and trains agents on:

- Schema reasoning  
- Metric definition grounding  
- SQL execution correctness  
- Evidence citation  
- Error recovery  

That is product-critical.

---

# 3️⃣ Why Existing Work Is Not Enough

## InsightBench
Strong for structured insight evaluation.  
But:
- No live SQL execution loop  
- No iterative correction  
- No schema complexity stress testing  

## DRBench
Strong for long-horizon document reasoning.  
But:
- No structured DB grounding  
- No SQL execution semantics  
- No metric fidelity evaluation  

## Text-to-SQL Benchmarks (Spider, BIRD, etc.)
Strong for SQL generation accuracy.  
But:
- No business-definition grounding  
- No doc-based metric interpretation  
- No analytics workflow  
- No iterative debugging loop  

---

# 4️⃣ What DataOps-Gym Actually Is

An interactive environment:

```python
state = {
    "schema": relational_db,
    "docs": business_definitions,
    "question": executive_query
}

### gent tools:
generate_sql()
execute_sql()
search_docs()
reflect_on_error()
generate_report()

### Environment returns:
SQL execution results
Runtime errors
Table previews
Constraint violations
Evaluation signals

This enables iterative reasoning, not single-shot prompting.
