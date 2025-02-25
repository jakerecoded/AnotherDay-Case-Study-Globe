# Interactive Case Study Globe Visualization

## Overview

This code creates an interactive 3D globe visualization that displays case studies as interactive points across the world map. When a user hovers over a point, a tooltip appears showing information about the case study including an image, title, and location. Clicking either the point or the tooltip opens the case study in a new tab.

## Technologies Used

- **three.js**: A JavaScript 3D library that provides the core 3D rendering capabilities
- **globe.gl**: A high-level library built on top of three.js that simplifies creating interactive globe visualizations
- **HTML/CSS**: For structuring and styling the visualization and tooltips
- **Vanilla JavaScript**: For implementing the interactive behavior and DOM manipulation

## Key Features

- **Interactive 3D Earth**: A smooth, rotating globe with markers at specific locations
- **Custom Markers**: Teal circular points representing case study locations
- **Responsive Tooltips**: Information cards that appear on hover with smooth fade-in transitions
- **Click Navigation**: Points and tooltips are clickable and navigate to detailed case studies
- **Hover Persistence**: Tooltips remain visible when hovering over them directly
- **Automatic Rotation**: The globe rotates automatically but pauses when interacting with markers
- **Responsive Design**: Adjusts to different screen sizes to maintain proper display

## Implementation Details

1. **Marker Data Structure**: Each case study is represented by a JavaScript object containing:
   - Title of the case study
   - Geographic location name
   - Latitude and longitude coordinates
   - Thumbnail image URL
   - URL to the full case study

2. **Globe Configuration**:
   - Transparent background for seamless integration with the page
   - Earth texture mapped to a sphere
   - Automatic rotation with user interaction override
   - Interactive camera controls with disabled zoom

3. **Tooltip System**:
   - Custom tooltips using HTML/CSS for rich formatting
   - Background gradient styling for modern appearance
   - Carefully structured layout with image and text sections
   - Hover state tracking to prevent unwanted tooltip dismissal

4. **User Interaction Logic**:
   - Mouse hover detection for showing tooltips
   - Click event handling for navigation
   - Delay timers to improve user experience when moving between elements
   - Global hover state tracking to control globe rotation behavior

## How It Works

1. The code initializes a globe.gl instance within a container element
2. Case study markers are positioned at their geographic coordinates
3. Event listeners handle mouse interactions (hover, click)
4. When hovering over a marker, a tooltip is dynamically created and positioned
5. The tooltip displays the case study's image, title, and location
6. Both markers and tooltips are clickable and direct users to the related URL
7. Mouse events track when the user is hovering over elements to ensure tooltips remain visible when needed
8. Globe rotation pauses during user interaction for better usability

## Browser Compatibility

Works in all modern browsers that support modern JavaScript, CSS, and WebGL, including:
- Chrome
- Firefox
- Safari
- Edge

## Integration Notes

The visualization can be integrated into any web page or content management system by including the required scripts, styles, and HTML container element. It's designed to be modular and self-contained.
