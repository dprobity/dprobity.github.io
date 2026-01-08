# Strategic Proposal Factory: Multi-Agent RAG for Federal RFPs

## 1. Executive Summary
The **Strategic Proposal Factory** is an enterprise-grade Multi-Agent Orchestration system designed to automate high-stakes grant proposals (USAID, GAVI, and Federal RFPs). By combining a **Hybrid Graph-Vector Memory** architecture with **McKinsey-grounded strategic frameworks**, the system resolves the "Capacity Gap" in non-profit business development. 

This project prioritizes **Data Sovereignty** and **Evaluation Rigor**, utilizing an internal "M&E for AI" layer to ensure all generated narratives are compliant, grounded, and strategic.

---

## 2. System Architecture
The system is built on a directed acyclic graph (DAG) using **LangGraph** to manage stateful, multi-turn interactions.



### Core Workflow:
1. **Ingestion Interface:** Layout-aware parsing of 100+ page RFP PDFs.
2. **Knowledge Processing:** Dual-store indexing (Neo4j for structural entity relationships and Pinecone/Supabase for semantic embeddings).
3. **Strategic Architect Agent:** Deconstructs requirements into a McKinsey **Issue Tree**.
4. **Synthesis Writer Agent:** Generates narratives using the **Pyramid Principle** (Answer-First logic).
5. **Red Team Auditor:** A conditional logic gate that audits drafts against the Compliance Matrix.
6. **Human-in-the-Loop:** A secure review interface for Program Leads to validate agent outputs before final export.

---

## 3. Technical Implementation Details

### Stateful Orchestration (LangGraph)
The system maintains a shared `AgentState` to ensure context continuity across massive document contexts. 

```python
class AgentState(TypedDict):
    rfp_text: str                   # Raw extracted content
    compliance_matrix: List[Dict]   # Shredded Section L/M requirements
    issue_tree: Dict                # McKinsey-style logic skeleton
    retrieved_context: Annotated[List[str], operator.add] 
    graph_entities: List[Dict]      # Neo4j entity mappings
    is_red_team_approved: bool      # Logic gate for final export
