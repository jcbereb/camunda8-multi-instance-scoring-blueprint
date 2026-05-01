# Dynamic Multi-Instance Scoring Blueprint (Camunda 8)

This repository contains an advanced executable pattern for orchestrating credit scoring processes using **Camunda 8**.
The blueprint demonstrates how to transform raw data into actionable collections, evaluate complex business rules using **DMN**, and dynamically manage human intervention.

## 🚀 Implemented Patterns

*   **Script Task Transformation**: Using FEEL expressions to map and clean data collections (JSON) from external services.
*   **Parallel Multi-Instance**: Iterative processing of client collections.
*   **DMN-Driven Routing**: Automated decision logic to determine the score level.
*   **Dynamic User Task Assignment**: Automatic assignment of tasks to specific groups based on the scoring evaluation result.

## 📂 Project Components

1.  **BPMN (`process-scoring.bpmn`)**: Main orchestrator that handles the logic for data preparation, evaluation, and user tasks.
2.  **DMN (`determine-scoring.dmn`)**: Decision table with hit policy `FIRST` to classify clients into categories: *Premium, Standard, High Risk or No Profile*.
3.  **Camunda Form (`scoring-result.form`)**: Dynamic form that uses text components with FEEL expressions to display the data of the current item in the iteration.
4.  **Test Payload (`test-payload.json`)**: File with sample data ready to start an instance and validate multi-instance logic.

### Requirements
*   Camunda 8 (Self-Managed o SaaS).
*   Modeler 5.40+.

---
Created by **Juan Carlos** - Camunda Champion & Chapter Leader Peru.
