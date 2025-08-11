# DataStar - Multidimensional Data Visualizer Terminal

<div align="center">

![DataStar Terminal](https://img.shields.io/badge/DataStar-v0.1.0-orange?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjIwIiBoZWlnaHQ9IjIwIiByeD0iNCIgZmlsbD0iIzBhMGEwYSIgc3Ryb2tlPSIjZTg4ZDM0IiBzdHJva2Utd2lkdGg9IjIiLz4KPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNiIgZmlsbD0iIzk3OTlmZSIvPgo8L3N2Zz4K)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-r128-000000?style=for-the-badge&logo=three.js&logoColor=white)
![WebGL](https://img.shields.io/badge/WebGL-2.0-990000?style=for-the-badge&logo=webgl&logoColor=white)

*A powerful, multidimensional data visualization platform developed by LATENT•SPACECRAFT, inspired by the artwork of Michael Okuda*

</div>

## **✶ Overview**

DataStar is a browser-based data visualization terminal that transforms CSV data into stunning 2D, 3D, 4D, 5D, and 6D visualizations. Built with a distinctive retrofuturistic aesthetic reminiscent of classic sci-fi interfaces and developed by LATENT•SPACECRAFT, it provides powerful visualization capabilities without requiring coding experience.

### ✨ Key Features

- **🎨 Retrofuturistic UI**: Inspired by Star Trek: TNG interface
- **📊 Multiple Visualization Modes**: 2D plots, interactive 2D arrays, 3D point clouds, 4D time-lapse animations
- **🌈 6-Dimensional Support**: X, Y, Z positioning + Color, Size, and Time dimensions
- **🖱️ Interactive Controls**: Manual camera rotation/zoom for 2D arrays, 3D, and 4D modes
- **📅 Smart Data Detection**: Automatic numerical, categorical, and datetime parsing with proper temporal ordering
- **⚡ Real-time Rendering**: WebGL-accelerated graphics with Three.js and custom particle shader
- **🎛️ Animation Controls**: Variable speed sliders and temporal navigation for 4D datasets
- **📊 Advanced Axis System**: Extended labeled axes with categorical value support and data type indicators
- **🔍 Data Filtering**: Real-time range sliders for numerical data and checkbox filters for categories, autoscaling axes
- **📤 Export Capabilities**: PNG images, 3D mesh (.obj), animated GIFs (4D data), and filtered CSV export
- **✨ Particle Effects**: Sophisticated particle system with shimmer effects and lifetime management
- **🔧 Modular Architecture**: Easily extensible for new visualization types

## 🏗️ Architecture

### Core Components

```
DataStar/
├── DropViz Class           # Main drag-drop application controller
├── Visualization Engine    # Three.js rendering system with particle effects
├── Data Processing         # CSV parsing, filtering, and normalization
├── Interactive Controls    # Mouse/touch camera manipulation
├── Particle System         # Advanced 4D animation with fade effects
├── Filter System           # Real-time data range and category filtering
├── UI Controller           # Event handling and user interaction
└── Export System           # PNG, OBJ, GIF, and CSV export functionality
```

### Class Structure

```javascript
class DropViz {
    constructor()              // Initialize application
    init()                     // Setup event listeners and Three.js
    
    // Data Management
    processFile(file)          // Parse CSV files with PapaParse
    populateDimensionSelectors() // Update UI with available dimensions
    updateDataPreview()        // Display data sample and headers
    
    // Visualization Methods
    create2DVisualization()    // 2D scatter plots
    create2DArrayVisualization() // Height-mapped grid cubes
    create3DVisualization()    // 3D point clouds with rotation
    create4DVisualization()    // Time-lapse animations
    
    // Three.js Management
    initializeThreeJS()        // Setup scene, camera, renderer
    animate()                  // Main render loop
    addAxisLines()             // 2D axis visualization
    add3DAxisLines()           // 3D axis visualization
    
    // Export Functions
    exportPNG()                // Canvas-to-image export
    exportMesh()               // OBJ format 3D export
}
```

## 📋 Current Implementation Status

### ✅ Completed Features

- [x] **Core UI Framework**: Retrofuturistic styling with CSS Grid layout and LATENT•SPACECRAFT branding
- [x] **File Processing**: Drag-and-drop CSV parsing with PapaParse and comprehensive data validation
- [x] **2D Visualization**: Interactive scatter plots with axis lines and color coding
- [x] **2D Array Visualization**: Interactive grid-based height mapping with manual camera controls
- [x] **3D Visualization**: Point clouds with full camera manipulation (rotation/zoom)
- [x] **4D Visualization**: Advanced particle-based time-lapse animations with fade effects
- [x] **5D/6D Support**: Color and size dimensions for enhanced data representation
- [x] **Smart Data Detection**: Automatic numerical, categorical, and datetime parsing with temporal ordering
- [x] **Interactive Controls**: Comprehensive mouse/touch rotation and zoom for all 3D modes
- [x] **Advanced Axis System**: Extended labeled axes with data type indicators and range labels
- [x] **Categorical Support**: Full grouping and visualization of non-numerical data
- [x] **Particle System**: Sophisticated 4D animation with shimmer effects and lifetime management
- [x] **Data Filtering**: Real-time range sliders and category checkboxes with live preview
- [x] **Animation System**: Robust temporal navigation with variable speed controls
- [x] **Data Preview**: Real-time header analysis and filtered sample display
- [x] **Dimension Management**: Dynamic selector population with type validation
- [x] **Export System**: PNG, OBJ mesh, animated GIF, and filtered CSV export
- [x] **Error Handling**: Comprehensive validation and user feedback system
- [x] **Responsive Design**: Dynamic viewport scaling and adaptive layout
- [x] **Performance Optimization**: Efficient particle systems and memory management

### 🪰 Known Bugs (Remedying is top priority)
- GIF Export freezes browser
- Color mapping for 2D Arrays fails

### 🔄 In Progress Features

- [ ] **Value Hover Display**: Point inspection with data value tooltips
- [ ] **Color Schemes**: Common color palettes and palette brewer
- [ ] **Advanced Interactions**: Point selection and highlighting system

## 💫 Release v0.1.0 - Current Features

DataStar v0.1.0 represents a fully functional, production-ready data visualization platform with the following capabilities:

### 🎨 **Visualization Modes**
- **2D Scatter Plots**: Traditional X/Y plotting with interactive controls
- **2D Interactive Arrays**: Height-mapped cube grids with full 3D camera manipulation
- **3D Point Clouds**: Full 6-dimensional data representation (X, Y, Z, Color, Size, Time)
- **4D Animations**: Advanced particle-based temporal visualization with fade effect

### 🎛️ **Control Systems**
- **Data Filtering**: Real-time numerical range sliders and categorical checkboxes
- **Animation Controls**: Variable speed 4D temporal navigation (0.01s - 5.0s intervals)
- **Camera Manipulation**: Mouse/touch rotation and zoom for all 3D visualizations
- **Auto-rotation Toggle**: Automatic camera movement for presentation mode

### 📊 **Data Intelligence**
- **Smart Detection**: Automatically identifies numerical, categorical, and datetime columns
- **Temporal Ordering**: Proper chronological sorting for datetime data in animations
- **Mixed Data Support**: Seamlessly handles datasets with multiple data types
- **Real-time Validation**: Comprehensive error checking and user feedback

### 📤 **Export Capabilities**
- **PNG Export**: High-resolution static image export
- **3D Mesh Export**: OBJ format for 3D modeling applications
- **Animated GIF**: True GIF generation for 4D animations
- **Filtered CSV**: Export current filtered dataset

### 🎯 **Planned Enhancements**

- [ ] **Statistical Overlays**: Regression lines, confidence intervals, clustering
- [ ] **Value Hover Display**: Interactive point inspection with data tooltips
- [ ] **Network Graphs**: Node-link diagrams for relationship data
- [ ] **Heatmaps**: 2D density and correlation matrices
- [ ] **Color Schemes**: Multiple palettes and custom color mapping
- [ ] **Collaborative Features**: Shareable visualization URLs
- [ ] **Data Transforms**: Built-in preprocessing and normalization options

## 🛠️ Development Setup

### Prerequisites

- Modern web browser with WebGL 2.0 support
- Text editor or IDE (VS Code recommended)
- Basic understanding of JavaScript ES6+
- Familiarity with Three.js (helpful but not required)

### Dependencies

The application uses CDN-hosted libraries for easy deployment:

```html
<!-- Three.js for 3D rendering -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>

<!-- PapaParse for CSV processing -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/PapaParse/5.3.0/papaparse.min.js"></script>

<!-- Google Fonts for typography -->
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&display=swap" rel="stylesheet">
```

### Quick Start

1. **Clone or download** the HTML file
2. **Open in browser** - no build process required (*Tested on Safari 18.6, Chrome 138.x, Edge 139.x*)
3. **Drop a CSV file** to begin visualization
4. **Select dimensions** using the control panel
5. **Switch visualization modes** with the mode buttons

### Development Workflow

```bash
# For local development with live reload
python -m http.server 8000  # Python 3
# or
python -m SimpleHTTPServer 8000  # Python 2
# or
npx serve .  # Node.js

# Open browser to localhost:8000
```

## 🧪 Testing

### Test Data Format

DataStar expects "numpy-compliant" CSV files:
- **First row**: Column headers
- **Subsequent rows**: Numerical, categorical, or datetime data
- **No missing headers**: Each column must be named
- **Date Formats Supported**: ISO (YYYY-MM-DD), US (MM/DD/YYYY), European (DD/MM/YYYY), and common variations

### Sample Test CSV

```csv
Time,Temperature,Pressure,Humidity,Energy,Phase,Date
1,20.5,1013.2,45.0,150.3,Solid,2023-01-15
2,25.1,1012.8,48.5,165.7,Solid,2023-01-16
3,30.2,1011.5,52.1,180.2,Liquid,2023-01-17
4,35.8,1010.2,55.3,195.1,Liquid,2023-01-18
# ... more rows
```

### Test Scenarios

1. **2D Visualization**: Temperature vs Energy (linear correlation)
2. **3D Visualization**: Temperature/Pressure/Humidity (3D cloud with manual controls)
3. **4D Animation**: Use Time or Date dimension for temporal animation
4. **5D/6D**: Add Color (Phase) and Size (Energy) dimensions
5. **Categorical Data**: Phase transitions and categorical groupings
6. **DateTime Parsing**: Proper chronological ordering of date columns
7. **Mixed Data Types**: Numerical, categorical, and datetime in same dataset
8. **Edge Cases**: Single column, all categorical, empty cells, malformed dates

## 🎨 Visual Design System

### Sample UI Color Palette

```css
:root {
    --primary-orange: #e88d34; /*UI Scaffold*/
    --primary-lilac: #9799fe; /*Labels*/
    --secondary-lavender: #d099d0; /*Raw Data*/
    --accent-yellow: #efa937;
    --accent-rose: #cd5f5e; /*User Input*/
    --bg-dark: #000000; /*Background*/
    --bg-panel: #000000; /*Panel Background*/
    --text-primary: #e88d34; /*Primary Text*/
    --text-secondary: #fc5f2c; /*Secondary Text*/
    --grid-color: #333333;
}
```

### Typography

- The *"Two Weekends Sans"* font by T. X. Zhang is redistributed here under its original [license](OFL.md).


## 🔧 Extension Guide

### Adding New Visualization Types

1. **Create Visualization Method**:
```javascript
createMyNewVisualization(dimensions) {
    // Clear existing scene objects
    while (this.scene.children.length > 2) {
        this.scene.remove(this.scene.children[2]);
    }
    
    // Process data and create geometry
    const geometry = new THREE.BufferGeometry();
    // ... your visualization logic
    
    // Add to scene
    this.scene.add(meshOrPoints);
    
    // Update status
    this.updateStatus('NEW VISUALIZATION: X OBJECTS RENDERED');
}
```

2. **Add UI Controls**:
```html
<button class="viz-button" data-mode="my-new-mode">My Viz</button>
```

3. **Update Switch Statement**:
```javascript
case 'my-new-mode':
    this.createMyNewVisualization(xDim, yDim, ...);
    break;
```

### Adding Data Processing Features

```javascript
// Example: Data filtering
filterData(dimension, minValue, maxValue) {
    return this.data.filter(row => {
        const value = row[dimension];
        return typeof value === 'number' && 
               value >= minValue && 
               value <= maxValue;
    });
}

// Example: Statistical calculations
calculateStats(dimension) {
    const values = this.data
        .map(row => row[dimension])
        .filter(v => typeof v === 'number');
    
    return {
        mean: values.reduce((a, b) => a + b) / values.length,
        min: Math.min(...values),
        max: Math.max(...values),
        std: Math.sqrt(values.reduce((sq, n) => sq + Math.pow(n - mean, 2), 0) / values.length)
    };
}
```

### Adding Export Formats

```javascript
exportCustomFormat() {
    // Generate custom format data
    const customData = this.generateCustomFormat();
    
    // Create download
    const blob = new Blob([customData], { type: 'application/custom' });
    const link = document.createElement('a');
    link.download = `dropviz_export_${Date.now()}.custom`;
    link.href = URL.createObjectURL(blob);
    link.click();
    
    this.updateStatus('CUSTOM EXPORT COMPLETE');
}
```

## 🐛 Known Issues & Limitations

### Current Limitations

1. **Memory Usage**: Large datasets (>10k points) may impact performance
2. **Mobile Support**: Experimental--Touch controls partially implemented for 3D
3. **Browser Storage**: No persistence between sessions
4. **Advanced Date Formats**: Some exotic date formats may require preprocessing

### Performance Considerations

- **Point Cloud Limits**: Optimal performance with <5000 points; tested with up to 130MB CSV files
- **DateTime Processing**: Large date columns may have slight parsing overhead

### Browser Compatibility

- **WebGL 2.0**: Required for Three.js rendering
- **ES6+ Features**: Modern JavaScript syntax used throughout
- **File API**: For drag-and-drop file handling
- **Canvas API**: For PNG export functionality

## 🤝 Contributing

### Code Style

- **ES6+ Syntax**: Use modern JavaScript features
- **Consistent Naming**: camelCase for variables, PascalCase for classes
- **Modular Design**: Keep methods focused and reusable
- **Error Handling**: Always validate inputs and provide user feedback

### Pull Request Process

1. **Fork** the repository
2. **Create feature branch**: `git checkout -b feature/amazing-viz`
3. **Test thoroughly** with various CSV formats
4. **Update documentation** for new features
5. **Submit pull request** with clear description

## 📈 Roadmap

### Phase 1: Core Stability (Current)
- ✅ Basic visualization modes
- ✅ File processing pipeline
- ⚠️ Export functionality (GIF broken)
- 🔄 Performance optimization
- 🔄 Mobile responsiveness

### Phase 2: Enhanced Interactivity
- ✅ Manual camera controls
- ✅ Real-time filtering and brushing
- 🎯 Data point selection and highlighting
- 🎯 Collaborative sharing features

### Phase 3: Advanced Analytics
- 🎯 Statistical model overlay
- 🎯 Machine learning integration
- 🎯 Time series analysis tools
- 🎯 Network analysis capabilities w/ JS

## 🔒 Security

### File Processing
- **Client-side Only**: **No data upload**, all processing in browser on-device
- **File Type Validation**: Only CSV files accepted
- **Size Limits**: Consider implementing file size restrictions
- **Content Sanitization**: PapaParse handles malformed CSV safely

### XSS Prevention
- **No Dynamic HTML**: Data displayed in controlled contexts
- **CSV Content**: Treated as data, not executable code
- **User Input**: Minimal attack surface with file-only input

## 📄 License

This project is open source and available under the [GPLv3 License](LICENSE).

---

<div align="center">

**EXCELSIOR**

[Report Bug](https://github.com/latent-spacecraft/datastar/issues) · [Request Feature](https://github.com/latent-spacecraft/datastar/issues) · [Contribute](https://github.com/latent-spacecraft/datastar/pulls)

</div>