# Functional and Non-Functional Requirements - Module 01

## NF

### REQ_NF_SW_LOG_001

#### Title
Log History Persistence

#### Description
The system must maintain the history of log messages, ensuring the persistence of recent events even when pre-set size thresholds are exceeded.

#### Traceability
- [SSS_NF_SW_LOG_001](SSS_M01.md#SSS_NF_SW_LOG_001)

---

## F

### REQ_F_GUI_UX_001

#### Title
Custom Pen Color Addition

#### Description
The user shall be able to add custom pen colors to the existing toolbar selection. 

#### Details
- A "+" icon shall be placed to the right of the existing pen color selectors.
- Clicking the "+" icon shall trigger a modal window for color configuration.
- The user must define a color pair: one for white background and one for black background.
- The system must validate and save the new color pair.
- The new color shall be immediately available for selection in the toolbar.
- The color adaptation mechanism (automatically switching colors based on background change) must apply to the newly added custom colors.

#### Traceability
- [SSS_F_GUI_UX_001](SSS_M01.md#SSS_F_GUI_UX_001)