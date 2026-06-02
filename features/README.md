# Requirements and Specifications Documentation - OpenBoardJ

OpenBoardJ traceability section. This folder has been introduced to manage the evolution of functionalities in a structured way, facilitating code maintenance and communication between developers.

## Purpose

The goal of this folder is to document requirements, constraints, and technical specifications before their implementation in the project core. This ensures that every change is planned, traceable, and consistent with the philosophy of the original software.

## File Coding

Files are organized by module (e.g., `M01` for the first module analyzed) and category:

* `REQ_Mnn.md`: **Requirements**. Define *what* the system must do from a functional or non-functional perspective.
* `SSS_Mnn.md`: **Software System Specifications**. Define *how* the requirement is technically implemented.
* `CON_Mnn.md`: **Constraints**. Define environmental or technological limits that influence development (e.g., performance, I/O, compatibility).

## Naming Convention

Each entity is identified by a unique code in the format:
`{TYPE}_{CAT}_{AREA}_{SUB}_{NNN}`

* **TYPE**: `REQ` (Requirement), `SSS` (Specification), `CON` (Constraint).
* **CAT**: `F` (Functional), `NF` (Non-Functional).
* **AREA**: System category (e.g., `SW` for software, `DB` for database, `GUI` for interface).
* **SUB**: Optional sub-category (e.g., `LOG` for logging, `UX` for user experience).
* **NNN**: Three-digit numeric counter.

## Analysis and Traceability Protocol

To ensure the integrity of the project, we follow a bidirectional traceability protocol:

1. **Definition**: Every new requirement (`REQ`) must be associated with a specification (`SSS`) that describes its implementation.
2. **Constraints**: Constraints (`CON`) serve as the basis for validating specifications.
3. **Hypertext Tracing**: Each file contains direct links to related elements.
* `REQ`s link to their respective `SSS`s.
* `SSS`s link to their reference `REQ`s and `CON`s.
* `CON`s remain independent (they define the perimeter).



## Contributions and Workflow (Issue-based)

To keep the project organized, we do not accept direct changes to the documentation files unless through the review process via **Issue**:

1. **Open an Issue**: If you want to propose a new requirement or modify an existing one, open a new *Issue* in the repository.
2. **Proposal Template**: In the issue, include:
* **Coding**: The requirement code (e.g., `REQ_NF_SW_LOG_001`).
* **Description**: A brief explanation of the need.
* **Documentation**: The text in Markdown format that you would like to see in the `REQ_Mnn.md`, `SSS_Mnn.md`, or `CON_Mnn.md` files.
* **Impact**: Indicate which files/specifications would be affected.


3. **Validation**: The proposal must be validated; any changes or clarifications will be discussed directly in the issue comments.
4. **Acceptance/Closure**:
* **Accepted**: The proposal is integrated into the official files, and the Issue is closed with a link to the update commit.
* **Rejected**: The Issue is closed with the reasoning behind the decision, keeping the history for future reference.