# Software System Specifications - Module 01

## NF

### SSS_NF_SW_LOG_001

#### Title
Log History Persistence

* When the 10MB threshold is exceeded, the log file must be truncated while preserving the last 33% of the current content. The operation must be atomic and configurable via startup parameter or configuration file.

#### Traceability
- [REQ_NF_SW_LOG_001](REQ_M01.md#REQ_NF_SW_LOG_001)
- [CON_NF_SW_LOG_001](CON_M01.md#CON_NF_SW_LOG_001)

---

## F

### SSS_F_GUI_UX_001

#### Title
Custom Pen Color Implementation

#### Technical Implementation
- **UI Component**: Extend the existing toolbar layout. Dynamically append a `QPushButton` (or equivalent) with a "+" icon to the color selection container.
- **Color Selection Dialog**: Implement a `QColorDialog` (or custom widget) that requires the user to input two values: `color_white_bg` and `color_black_bg`.
- **Data Persistence**: Store the custom color pairs in the application settings (e.g., QSettings or a local JSON configuration file) to ensure persistence across sessions.
- **Rendering Logic**: Hook into the existing `ThemeManager` or `ColorAdapter` service. When the background mode toggles (White <-> Black), the application must iterate through the custom color palette and apply the corresponding mapping defined during the addition process.

#### Traceability
- [REQ_F_GUI_UX_001](REQ_M01.md#REQ_F_GUI_UX_001)
- [CON_F_GUI_UX_001](CON_M01.md#CON_F_GUI_UX_001)