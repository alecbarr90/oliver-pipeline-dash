# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
- Single-file React application (index.html) with embedded JSX
- Uses React, Tailwind CSS, Recharts, and Babel from CDN
- Client-side only with localStorage for data persistence
- Pipeline and resource allocation dashboard for agency team management
- Features project tracking, team capacity visualization, and revenue projections

## Development Commands
- Open `index.html` directly in a browser to view the application
- No build, lint, or test commands as this is a single-file app
- Use browser dev tools for debugging

## Code Style Guidelines
- **JSX**: Standard React syntax with self-closing tags where appropriate
- **Naming**: camelCase for variables/functions, PascalCase for components
- **Formatting**: 2-space indentation
- **Components**: Functional components with React Hooks (useState)
- **Styling**: Tailwind utility classes directly in JSX + custom CSS classes for neubrutalism design
- **Error Handling**: Try/catch blocks for any operations that may fail
- **State Management**: Keep state at highest necessary level
- **Comments**: Include comments for complex logic or component purposes

## Design System
- **Neubrutalism**: Thick black borders (2px), flat bold colors, subtle drop shadows
- **Status Pills**: Consistent styling with thick borders and status-specific colors
- **Buttons**: Bold text, thick borders with shadows for clear affordance
- **Cards**: White background with thick borders and subtle shadows
- **Inputs**: White background with thick borders for form elements
- **Typography**: Clear hierarchy with consistent font sizes and weights

## Chart Styling Guidelines
- Use ResponsiveContainer for all Recharts components
- Pie chart labels: 6px font size, positioned around outer rim
- Monetary values shown in £k format
- Capacity bars: Equal width segments for allocations with appropriate category colors
- Utilization percentage labels: Bold white text for visibility
- Consistent color schemes:
  - Project categories: Fixed colors defined in projectCategories array
  - Status colors: Green for Confirmed, Blue for Ongoing, Yellow for Pending, Purple for Pitch

## Data Structures
- **Team Members**: Name, role, capacity, allocations to projects
- **Projects**: Name, status, value, timeline, category assignments
- **Categories**: Fixed category system with ID, name, and color properties
- **Semblance Opportunities**: Client, status, monetary value, notes

## Feature Implementation Notes
- New allocations use randomly selected colors from existing categories
- Tooltips provide detailed information for complex data (time calculations, etc.)
- Edit mode is section-specific rather than global
- Time calculations are shown in days per week
- Monetary values are displayed in thousands (£k)