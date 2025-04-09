# Active Context: Oliver Pipeline Dashboard

## Current Work Focus
The current focus is on enhancing the dashboard with an editable interface that allows users to modify data directly within the application. This includes:

1. Implementing an "Edit Mode" toggle for each dashboard section
2. Adding form controls for data editing
3. Creating a category management system for project allocations
4. Ensuring visual consistency between edit and view modes

## Recent Changes

### Capacity Visualization Enhancements
- Updated capacity bars to show projects as equal segments with category colors
- Removed 100% capacity vertical line markers for cleaner visuals
- Changed all utilization percentage labels to be bold and white for visibility
- Added informational tooltips to explain time calculations

### Pie Chart Improvements
- Standardized all pie chart labels to 6px font size for consistency
- Updated Semblance Opportunity Status chart to display monetary values (£k) instead of counts
- Fixed pie chart label rendering for better visibility
- Enhanced tooltip formatting for clearer data interpretation

### Visual Styling Updates
- Applied consistent neubrutalism design across all UI components
- Improved status pills and button styling with thick borders and drop shadows
- Enhanced text legibility on colored backgrounds
- Implemented color randomization for new project allocations

## Next Steps
1. Test and refine the category management functionality
2. Implement data validation for form inputs
3. Add confirmation dialogs for destructive actions
4. Consider adding data persistence options

## Active Decisions and Considerations

### Category Management Approach
- Using a centralized categories array with unique IDs
- Referencing categories by ID in allocation objects
- Providing fallback colors for allocations without categories

### Edit Mode UX Decisions
- Section-specific edit modes rather than global edit mode
- Inline editing rather than modal dialogs
- Immediate visual feedback for changes

### Color System
- Using distinct colors for different categories
- Maintaining color consistency across different visualizations
- Using color to indicate status (red for over-capacity, green for healthy)

## Learnings and Project Insights

### React State Management
- Using temporary state storage for edit mode
- Managing complex nested state updates
- Handling cancellation by storing original data

### Visualization Techniques
- Grouping data by category for pie charts
- Handling overflow in capacity visualizations
- Using color effectively to convey information

### UX Patterns
- Balancing information density with clarity
- Providing clear visual cues for edit mode
- Ensuring consistent interaction patterns
