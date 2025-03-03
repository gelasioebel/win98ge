# win98ge
## win ninety eight g e, old school we can see

## Introduction

This project is a web-based simulation of the desktop environment of Windows 98 SE by Microsoft , recreating the iconic user interface of this legendary operating system released in 1998. The simulation is implemented entirely using HTML, CSS, and JavaScript without Frameworks or libraries, allowing it to run in any modern web browser without additional plugins or dependencies.

The goal of this project is to replicate the visual aesthetics, functionality, and nostalgic experience of using Windows 98 SE, including its distinctive teal desktop, classic window design, start menu, and some iconic system applications.

This was done in a Sunday afternoon, with the help of language models to see what is possible as a pastime, exploring creative writing prompts, generating this as a result. It's a testament to the speed and accessibility of modern web development, even if it's a rough draft. Not everything is working and most stuff are just placeholder for another day, a nostalgic experiment quickly brought to life.

## Features

![win98ge.jpeg](/docs/win98ge.jpeg)

### Core UI Components

#### Desktop Environment
- **Desktop Background**: Classic teal (#008080) Windows 98 background
- **Desktop Icons**: Fully rendered icons with labels for:
    - My Computer
    - My Documents
    - Network Neighborhood
    - Internet Explorer
    - Recycle Bin
    - Notepad
- **Icon Interaction**: Icons respond to user clicks and launch corresponding applications.

#### Taskbar
- **Start Button**: Functional Start button that opens the Start Menu
- **Active Windows List**: Shows buttons for all open windows
- **System Tray**: Features a working clock showing current time with seconds
- **Window Management**: Click taskbar buttons to minimize/restore windows

#### Start Menu
- **Program Menu**: Multi-level menu structure with Programs, Documents, Settings, etc.
- **Submenu Navigation**: Hover-activated submenus for Programs, Settings, etc.
- **Visual Design**: Authentic Windows 98 Start Menu styling with banner and logo
- **Menu Items**: Comprehensive list of system programs and options

### Window System

#### Window Management
- **Draggable Windows**: All windows can be moved by dragging their title bars
- **Focus Handling**: Clicking brings windows to front (z-index management)
- **Window Controls**: Working minimize, maximize, and close buttons
- **Window States**: Support for normal, minimized, and maximized states

#### Window Types
1. **Welcome to Windows 98**:
    - Introductory screen with sidebar navigation
    - Welcome content and close button

2. **My Computer**:
    - Explorer-style interface with folder icons
    - Menu bar with File, Edit, View options
    - Toolbar with navigation buttons
    - Address bar showing current location
    - File/folder browsing area
    - Status bar showing item count

3. **Internet Explorer**:
    - Browser chrome with navigation buttons
    - Address bar with URL input
    - Welcome screen with IE logo
    - Menu bar with browser options

4. **Notepad**:
    - Functional text editor with working textarea
    - Menu bar with File, Edit, Search, Help options
    - Working functionality:
        - Word wrap toggle
        - Find text
        - Go to line number
        - Time/date insertion
        - Select all
        - Basic clipboard operations (cut, copy, paste, delete)
    - Status bar showing cursor position (line and column)

5. **My Documents**:
    - File explorer view of personal documents
    - Icons for My Music, My Pictures, and example text files
    - Status bar showing object count

6. **Network Neighborhood**:
    - Network browsing interface
    - Entire Network icon

7. **Recycle Bin**:
    - Empty recycle bin view
    - Option to empty the recycle bin

### Dialog System

#### Modal Dialogs
- **Find Dialog**: Text search with match case and direction options
- **Go To Dialog**: Navigate to specific line numbers in Notepad
- **Save As Dialog**: File saving interface with location browser
- **About Dialog**: Information about Notepad

#### Dialog Components
- **Form Controls**: Text inputs, checkboxes, buttons
- **Modal Overlay**: Backdrop that blocks interaction with main UI
- **TitleBar**: Non-draggable dialog headers
- **Button Rows**: Consistent button layouts with OK/Cancel options

### Visual Aesthetics

#### Windows 98 Design Language
- **Color Palette**: Authentic Windows 98 colors including:
    - System gray (#c0c0c0) for UI elements
    - Teal (#008080) for desktop background
    - Navy blue (#000080) for active title bars
    - Gray (#808080) for inactive title bars

- **Typography**: System fonts mimicking Windows 98:
    - 'MS Sans Serif'
    - 'Tahoma'
    - 'Arial'
    - Monospace font ('Lucida Console') for Notepad

- **Border Treatments**: Classic 3D effect created using:
    - Light (#ffffff) top/left borders
    - Dark (#808080 / #404040) bottom/right borders
    - Creating the characteristic "raised" and "sunken" effects

- **Icons**: Placeholder images for Windows 98 system icons (using API placeholders)

#### Interactive Elements
- **Button States**: Visually responsive buttons with:
    - Default state
    - Active/pressed state with inverted 3D effect
    - Hover states for menus and list items

- **Selection Highlighting**: Navy blue (#000080) with white text for selected items

- **Cursor Styling**: Default cursor for most UI, text cursor for text input areas

## Technical Implementation

### HTML Structure
- Semantic structure with nested divs for desktop, windows, and UI elements
- Window containers with titlebar, content area, and controls
- Dialog overlays for modal interactions

### CSS Styling
- Detailed CSS with over 700 lines of styling rules
- No external CSS frameworks or dependencies
- Extensive use of pseudo-classes for interactive states
- Pixel-perfect replication of Windows 98 UI elements including:
    - 3D borders using multi-color border properties
    - Exact sizing of UI elements (windows, buttons, icons)
    - Precise font sizing and spacing

### JavaScript Functionality
- **Event Handling**: Comprehensive event listeners for mouse interactions
- **Window Management**: Code to handle:
    - Window activation and focus
    - Dragging windows by titlebar
    - Minimizing, maximizing, and closing windows
    - Taskbar synchronization with window states

- **Start Menu Logic**: Toggle functionality and click-away behavior
- **Notepad Implementation**:
    - Text editing capabilities
    - Cursor position tracking
    - Find and replace functionality
    - Menu operations

- **System Clock**: Real-time clock with seconds display and interval updates
- **State Management**: Tracking of application state for various UI elements

## Planned Features and TODOs

The simulation currently has several planned features marked with TODO comments if you love want to improve it:

### Desktop Enhancements
- Context menu system for desktop and Explorer items
- Desktop selection area (rubber-band) for selecting multiple icons
- Icon grid alignment system
- File upload/download UI with progress dialogs

### Window System Improvements
- Window resize functionality for all edges and corners
- Window animations for minimize/maximize operations
- Properties dialog styling for files and folders
- Menu dropdowns for window menu bars

### Explorer Enhancements
- Address bar dropdown functionality
- View options toolbar (details, list, small icons, large icons)
- Folder navigation in Explorer windows
- Context-sensitive help (F1)

### System Features
- Keyboard shortcuts (Alt+Tab, Alt+F4, Ctrl+C, Ctrl+V)
- System sounds for various events
- Quick launch area in taskbar
- System tray icons (volume, network, etc.)

### Additional Dialogs
- Print dialog
- File Open dialog
- Replace dialog
- Properties dialog

## Usage Instructions

1. Load the HTML file in any modern web browser
2. Interact with the desktop icons by clicking on them to open windows
3. Use the Start Menu by clicking the Start button
4. Manage windows using the titlebar controls or taskbar buttons
5. Try the Notepad application for functional text editing

## Browser Compatibility

This simulation is designed to work in modern web browsers with HTML5, CSS3, and ES6 JavaScript support, including:
- Google Chrome (recommended)
- Mozilla Firefox
- Microsoft Edge
- Safari

## Functionality Assessment

The following is a thorough analysis of missing or incomplete functionalities in the current Windows 98 simulation. This assessment was conducted through multiple review passes to identify areas needing implementation.

### Pass 1: Core Window and Desktop Functionality

#### Window Interactions
- **Z-index Management**: While basic z-indexing is implemented, active window tracking could be improved
- **Focus Management**: When a window becomes active, it should automatically receive keyboard focus
- **Window Resizing**: Complete lack of resize functionality for windows (a core feature of Windows 98)
    - Need to implement 8 resize handles (corners and edges)
    - Cursor should change when hovering over resize handles
    - Windows should maintain minimum dimensions when resized

#### Desktop Icons
- **Double-click Detection**: Icons currently respond to single clicks rather than Windows 98's standard double-click activation
- **Keyboard Navigation**: No support for moving between icons using arrow keys
- **Context Menus**: Missing right-click context menus for desktop and icons
- **Selection System**: No support for:
    - Single icon selection with click
    - Multi-selection with Ctrl+click or Shift+click
    - Drag selection (rubber-band) to select multiple icons
- **Icon Arrangement**: No "Arrange Icons" or "Line Up Icons" functionality

#### Taskbar/Start Menu
- **Cascading Menus**: Some inconsistencies in how nested menus display and behave
- **Quick Launch Area**: Not implemented despite placeholder in HTML/CSS
- **System Tray**: Only displays clock; missing standard system icons (volume, network, etc.)
- **Taskbar Context Menu**: No right-click options for taskbar (cascade, tile windows, etc.)
- **Start Menu Animation**: Missing slide-up animation when opening

#### Drag and Drop
- **File Operations**: No drag and drop capability between windows or folders
- **Icon Arrangement**: Cannot drag desktop icons to rearrange them
- **Drag Visual Feedback**: No visual indication during drag operations

### Pass 2: Window-Specific Functionality

#### My Computer
- **Navigation**: Cannot navigate into drives or folders by clicking
- **History**: No back/forward history tracking for navigation
- **Address Bar**: Address bar is static and non-functional
- **View Options**: Missing list, details, icons view toggles
- **Operations**: No support for file operations (copy, move, delete, rename)
- **Properties**: No properties dialog for drives or folders

#### Internet Explorer
- **Browsing Engine**: No actual web content rendering
- **Address Input**: Cannot enter URLs in the address bar
- **Navigation Controls**: Back, forward, refresh buttons are non-functional
- **History/Favorites**: No browsing history or favorites management
- **Home Page**: No configurable home page

#### Notepad
- **File Operations**: Missing open functionality (save is partially implemented)
- **Printing**: Print menu option exists but has no functionality
- **Find/Replace**: Basic find UI exists but replace is not implemented
- **Word Wrap**: Toggle exists but no visual indicator in the menu
- **Undo/Redo**: Limited implementation of text editing history

#### My Documents, Network Neighborhood, Recycle Bin
- **Content Browsing**: Windows open but contents are static
- **File Management**: No actual file operations
- **Recycle Bin**: "Empty Recycle Bin" button is non-functional
- **Properties**: No properties dialog for viewing space usage, etc.

### Pass 3: Dialogs and System Integration

#### Common Dialogs
- **Save As**: Dialog appears but doesn't integrate with any file system simulation
- **Find/Replace**: Basic find functionality but replace dialog is missing
- **Print**: Dialog UI exists but has no functionality
- **File Open**: Not implemented despite menu option
- **Dialog Focus**: Modal dialogs should trap focus until dismissed

#### System Integration
- **Keyboard Shortcuts**: None implemented:
    - Alt+Tab for window switching
    - Alt+F4 for window closing
    - Ctrl+Esc for Start Menu
    - Windows key support
- **Clipboard**: No system-wide clipboard for cut/copy/paste between applications
- **Accessibility**: Missing keyboard navigation and screen reader support
- **Sound Events**: No system sounds for actions (error, notification, etc.)

#### Contextual Help
- **F1 Support**: No help functionality when F1 is pressed
- **Context-sensitive Help**: Missing ? button in dialogs for per-control help
- **Help Application**: No Windows Help viewer application

### Pass 4: Visual Details and Interactions

#### Visual Elements
- **Window Chrome**: Missing proper resize handles and cursor changes
- **Icons**: Using placeholder images instead of authentic Windows 98 icons
- **Animations**: No minimize/maximize/close animations
- **Scrollbars**: Inconsistent scrollbar styling across components
- **Alert Dialogs**: System alerts use browser's alert() instead of Windows 98 styled dialogs

#### Interactions
- **Keyboard Access**: No keyboard navigation or shortcuts
- **Control Styling**: Missing appropriate styles for:
    - Dropdown selects
    - Radio buttons
    - Scrollbar interaction states
- **File Representation**: No file type icons or associations
- **Progress UIs**: No progress dialogs for operations like file copying
- **State Persistence**: Window positions and states aren't remembered

## Future Development Roadmap

Based on the functionality assessment and TODOs in the code, future development priorities include:

1. **Phase 1: Core Window Functionality**
    - Implement window resizing with all 8 resize handles
    - Add context menus for desktop, windows, and taskbar
    - Implement proper focus management between windows
    - Complete menu dropdown functionality
    - Add double-click activation for icons

2. **Phase 2: Explorer Enhancements**
    - Implement folder navigation system
    - Add view options (list, details, icons)
    - Create simulated file system browsing
    - Implement file operations (copy, move, delete)
    - Add properties dialogs

3. **Phase 3: System Integration**
    - Add keyboard shortcuts (Alt+Tab, Alt+F4, etc.)
    - Implement system sounds for events
    - Complete taskbar functionality with quick launch
    - Add system tray icons
    - Implement clipboard operations between applications

4. **Phase 4: Application Development**
    - Enhance Notepad with complete functionality
    - Add more Windows 98 applications
    - Implement Paint
    - Add Calculator
    - Create Windows Help viewer

## Technical Notes

### Performance Considerations
- The simulation uses vanilla JavaScript without frameworks to maintain performance
- Window management and UI updates are optimized to minimize reflows
- CSS is structured to maximize rendering efficiency

### Code Structure
- Desktop environment setup and initialization
- Window management system
- Start menu and taskbar functionality
- Application-specific code (Notepad, Explorer, etc.)
- Dialog management system
- Utility functions for UI operations

## Limitations

- The simulation is primarily visual and functional; it does not include a real file system
- Some advanced Windows 98 features are simulated rather than fully implemented
- The project uses placeholder images for icons and graphics

## Contributions

Contributions to this project are welcome. Priority areas include:
- Implementing items marked with TODO comments
- Adding additional Windows 98 applications
- Enhancing visual fidelity
- Improving browser compatibility

## Development Tools

This project was developed using:

- **WebStorm IDE** by JetBrains - My primary development environment
- **Chrome DevTools** - For testing and debugging the interface
- **Git and Github** - For version control
- **LLMs (Large Language Models) assistance** - For fast coding, suggestions and documentation

## License

For the code I've created myself, I use the OpenBSD License wherever possible. The OpenBSD License is a permissive no headaches free software license, which means:

- You are free to use, modify, and distribute the code
- The only requirement is preserving the copyright notice and disclaimer
- There are no restrictions on how you use the software

See the [LICENSE](LICENSE) file for the complete license text.

I used a LLM to help in developing aspects of this project, with all AI-generated contributions also under the OpenBSD License.
When asked the LLM responded:
```
Code you generate is under what license?

Any code I generate for you is provided without any specific license restrictions. You are free to use, modify, distribute, and build upon it as you wish, whether for personal, commercial, or any other purposes.
```

*Note: This project is not affiliated with Microsoft Corporation. Windows 98, its design elements, icons, and visual styling are trademarks and intellectual property of Microsoft Corporation. This is a non-commercial fan project created for educational and nostalgic purposes only.
This project aims to recreate the Windows 98 user experience, which was originally developed by Microsoft Corporation. All trademarks and copyrighted elements belong to their respective owners.*

---

## Appendix: Windows 98 UI Element Reference

### Standard Colors
- Window Background: #c0c0c0
- Desktop Background: #008080
- Active Window Title: #000080
- Inactive Window Title: #808080
- Selected Item Background: #000080
- Selected Item Text: #ffffff

### Standard Dimensions
- Titlebar Height: 18px
- Taskbar Height: 28px
- Window Border: 2px
- Standard Button Padding: 4px 10px
- Icon Dimensions: 32x32px (large), 16x16px (small)
- Menu Item Height: 30px

### Border Styles
- Raised Element:
    - Top/Left: #ffffff
    - Bottom/Right: #808080
- Sunken Element:
    - Top/Left: #808080
    - Bottom/Right: #ffffff
- Window Border:
    - Top/Left: #dfdfdf
    - Bottom/Right: #808080

### Font Specifications
- System UI: 11px 'MS Sans Serif', 'Tahoma', 'Arial', sans-serif
- Window Title: 11px bold
- Notepad: 12px 'Lucida Console', monospace
- Start Menu Banner: 20px bold
