# Technical Context: Oliver Pipeline Dashboard

## Technologies Used

### Frontend Framework
- **React**: Used for building the user interface components
- **JSX**: For writing component templates
- **React Hooks**: For state management (useState)

### UI Libraries
- **Tailwind CSS**: For styling and responsive design
- **Recharts**: For data visualization (bar charts, pie charts)

### Development Tools
- **Babel**: For JSX transpilation in the browser
- **CDN-hosted libraries**: All dependencies are loaded via CDN

## Development Setup

### Environment
- Single HTML file with embedded scripts
- No build process required
- Runs directly in the browser without a server

### Dependencies
- React and ReactDOM (production builds)
- Recharts for data visualization
- Tailwind CSS for styling
- Babel for JSX transpilation

### File Structure
```
/oliver-pipeline-dash
├── index.html       # Main application file
└── memory-bank/     # Documentation
```

## Technical Constraints

### Client-Side Only
- No backend server or database
- All data is stored in React state
- Changes are not persisted between page refreshes

### Browser Compatibility
- Requires modern browsers that support ES6+ features
- Relies on browser's ability to run Babel transpilation

### Performance Considerations
- Recharts rendering can be performance-intensive with large datasets
- State updates trigger re-renders of components

## Tool Usage Patterns

### React State Management
- Top-level state for main data structures
- State updates through setter functions
- Temporary state for edit mode

### Tailwind CSS Patterns
- Utility-first CSS approach
- Responsive design using Tailwind's breakpoint classes
- Custom styling for charts and visualizations

### Recharts Implementation
- ResponsiveContainer for adaptive sizing
- Consistent color schemes across chart types
- Custom tooltips and labels for better data presentation

### Edit Mode Implementation
- Toggle between view and edit modes
- Form controls for data editing
- Save/cancel functionality with state management
