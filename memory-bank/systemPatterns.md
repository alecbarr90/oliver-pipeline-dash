# System Patterns: Oliver Pipeline Dashboard

## Architecture Overview
The Oliver Pipeline Dashboard is built as a single-page application (SPA) using React with a component-based architecture. The application is entirely client-side, with no backend server, making it portable and easy to deploy.

## Key Components

### Dashboard Container
- Main container component that manages the overall state
- Handles view switching between different dashboard sections
- Maintains the global edit mode state

### Data Management
- Uses React's useState hooks for state management
- Implements a pattern for saving/canceling edits with temporary state storage
- Maintains original data during edit mode to support cancellation

### Visualization Components
- Leverages Recharts library for data visualization
- Implements responsive containers for different screen sizes
- Uses consistent color schemes across different chart types

## Design Patterns

### Edit Mode Pattern
- Toggle between view and edit modes
- Store original data when entering edit mode
- Provide save and cancel options
- Implement form controls appropriate for each data type

### Category Management System
- Centralized category definitions with IDs, names, and colors
- Reference categories by ID in allocation objects
- Fallback mechanism for allocations without category assignments
- Color consistency across different visualizations
- Fixed categories instead of dynamic management for simplicity
- Reliance on tooltips and legends rather than direct labels on pie charts

### Capacity Visualization Pattern
- Horizontal bar representation of capacity
- Color-coded segments based on project categories
- Overflow indication for over-capacity allocations
- Clear visual indicators for utilization percentages

### Data Transformation Patterns
- Transform raw data into chart-compatible formats
- Group allocations by category for pie charts
- Calculate derived values (e.g., utilization percentages, totals)
- Format currency and time values consistently

## Critical Implementation Paths

### Edit Mode Implementation
1. Toggle edit state with "Enter Edit Mode" button
2. Store original data in temporary state
3. Render editable form fields instead of static displays
4. Process updates on save or revert to original on cancel

### Category Management
1. Store categories with unique IDs, names, and colors
2. Reference categories in allocation objects
3. Use fixed categories with predefined colors
4. Ensure color consistency across visualizations

### Allocation Visualization
1. Calculate running totals for positioning
2. Handle overflow beyond capacity
3. Apply appropriate styling based on utilization
4. Display category information in legends
