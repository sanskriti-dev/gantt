### 6.3.5

- Fix the issue with task grouping which caused vertical scroll position to reset after moving any task with drag and drop
- Fix the script error which happened when drag_timeline config was set to null
- Fix the incorrect position of highlighted cells when static_background and static_background_cells are enabled and smart_rendering is disabled
- Fix the issue with the onAfterBranchLoading event not being called
- Fix the incorrect work of smart rendering when the value of task_height is less than the value of row_height
- A public method for rebuilding gantt layout after changing its config is added

### 6.3.4

- Fix crashes of the resource load diagram when smart rendering is switched off
- Fix issue with the custom task property named "unit", as gantt considered it as a duration unit value and multiplied the task duration after its dragging
- Fix the incorrect Tooltip position when the autosize config is enabled
- Fix the incorrect alignment behavior of grid cells when both the scrollable property and autofit config are set to true
- Creating a link between a task in the timeline and a placeholder in the grid is now blocked
- Fix the bug with the auto scheduling extension that caused gantt to freeze when a task has the constraint type (SNET/FNET/SNLT/FNLT) with no date specified, or with an invalid date

### 6.3.3

- Fix the incorrect resizing behavior of grid that disabled the Timeline in some cases
- gantt.parse should now correctly update the project tree when a parent task is loaded after its children
- Fix compatibility with SalesForce Lightning Aura components framework (Evaluation build)
- Fix the incorrect position of the Tooltip in SalesForce environment
- Fix the incorrect Tooltip position when the gantt container has a vertical margin
- Add missing WAI-ARIA attributes to elements inside the gantt
- Fix the incorrect work of the min_duration config
- Fix the incorrect work of link formatters with custom instances of the gantt

### 6.3.2

- Fix the script error which happened when gantt.destructor was called when the click-drag feature was enabled
- gantt.parse no longer modifies data objects passed into arguments, deep copies are made instead
- TypeScript type definitions were updated
- onBeforeBranchLoading and onAfterBranchLoading public events were added so it would be possible to modify the url or dynamic parameters of dynamic loading requests
- Added a public method for changing the url of the dataProcessor after its initialization

### 6.3.1

- Fix the regression in the smart rendering which caused links not to be rendered in some cases.
- Fix the bug that allowed modifying and creating new tasks with keyboard navigation when the read-only mode is activated
- Fix the display issue with Fullscreen extension which allowed some page elements to be displayed over the gantt in the fullscreen mode
- Fix the bug that caused the drag-timeline extension to reset the value of the readonly config

### 6.3

- Ability to specify decimal units for the duration of tasks
- Ability to scroll the timeline via mouse click and drag
- Ability to drag and drop multiple tasks horizontally

- Ability to display tasks outside the explicit start_date and end_date range of the time scale
- Add a new task_end_date template for formatting end dates of tasks
- Ability to add custom actions to the Undo stack
- Ability to connect custom layers to smart rendering
- Inline editors for predecessors now support formatted values of links
- Remove default limits for input values in date inline editors
- Ability to specify the root node for the Fullscreen extension
- Ability either to change or disable horizontal scroll by shiftKey+mousewheel
- Roboto font was removed from Material skin and has to be imported manually

- Fix crashes of the resource histogram when smart rendering is switched off
- Fix compatibility with r.js compressor
- Fix various conflicts between keyboard navigation and inline editors
- Fix the incorrect state of the DataProcessor when tasks and links were modified sequentially from a custom router
- A correct data object of Task/Link is now also passed into delete call of a custom router

### 6.2.7

- Fix the issue with vertical resizing of grids with horizontal scroll in complex layouts
- Fix the incorrect work of the resource histogram when the scale step is greater than one
- Fix the reopened bug with collapsed branches after calling gantt.parse from v6.2.4 bugfix

### 6.2.6

- Fix the regression in v6.2 Smart Rendering which in some cases caused incorrect vertical positions of tasks after re-initialization of the Gantt
- Fix the issue with QuickInfo popup not being displayed for unscheduled tasks
- Fix incorrect work of extension files with the Ultimate build of Gantt

### 6.2.5

- Fix incorrect initial values of subtasks in the onBeforeTaskChanged event handler after dragging a project with subtasks
- Fix incorrect work of the grouping extension when auto task types are enabled
- Fix the script error after returning the false value from the onTaskLoading event handler
- Add clearer error messages for the exceptions that can be thrown from gantt.load and gantt.parse

### 6.2.4

- Fix the issue with task branches being collapsed after updating data using gantt.parse
- Fix the incorrect work of smart rendering in the resource view
- Fix the issue which caused the Zoom module to attach redundant DOM event handlers on each re-initialization of the Gantt 

### 6.2.3

- Fix the incorrect work of the Constraint control in IE11 and MS Edge browsers
- Fix the size of the Gantt element in Fullscreen mode
- Fix the issue with onExpand and onCollapse events not being called from Fullscreen mode
- Correct the Tooltip position when the mouse pointer is near the left/right edge of the screen
- The Tooltip should now be hidden when the Lightbox is opened
- The Tooltip should now be hidden when the chart is scrolled
- Fix the incorrect work of Tooltip which caused the tooltip not to be updated when mouse pointer moved between two elements matching the same selector
- Fix the incorrect work of getTaskBy when null or 0 is provided as a second argument
- Fix the issue with WBS column not being updated after sorting the gantt
- Fix the incorrect display of static_background in Material skin

### 6.2.2

- Add the `gantt.license` property
- Add the `onLinkCreated` API event for new links, similarly to the `onTaskCreated` functionality for new tasks
- `gantt.moveTask` returns false when the action is prevented using onBeforeTaskMove
- Fix the issue which caused a link line to disappear when the render method is called while a user creates a new link
- Fix the issue when markers were not displayed when their start date was set earlier than the minimal date of the time scale
- Fix the issue when markers were not displayed when gantt was initialized with the `gantt.config.show_chart = false` config
- Fix a disappearing modal overlay of the lightbox when a user changed the type of a task
- Fix the issue in keyboard navigation presets, when onAfterTaskUpdate was fired after Shift+left arrow hotkey even if the action was canceled using onBeforeTaskMove

### 6.2.1

- Fix IE11 compatibility of the click-drag feature
- Fix the script error which happened when the user tried to add a new task into an empty chart with the resource view
- Fix the incorrect behavior of the grouping extension which caused assigning an incorrect group value to new tasks
- Fix a script error in the keyboard navigation extension thrown from the Alt+Arrow key shortcut
- Filtering in the resource control is changed to ignore text case
- Task dragging and drag-and-drop may finish on mouseup on any gantt element
- Fix the script error which happened after saving an unscheduled task

### 6.2.0

- Smart rendering is now embedded into the component
- Smart rendering works for rows and cells in all timelines
- static_background allows rendering highlighted cells
- Ability to expand/collapse split tasks (PRO)
- Add new Zoom module, add the ability to zoom by mousewheel
- New options for inline editors
- Simplified scales API
- Fix bug that caused multiple selected tasks to lose CSS classes after repaint
- Fix script error when destroying Gantt from data processor handler

### 6.1.7

- Fix incorrect behavior of getClosestWorkTime
- Fix issue with the autoscroll which happened after toggling visibility of the timeline
- Fix bug in the Multiselect extension which caused selected tasks to lose highlight after chart repaint
- Fix script error which happened after vertical drag-and-drop if smart rendering and keyboard navigation extensions were enabled
- Fix incorrect behavior which happened when users tried to switch between inline editors using the Tab key if some columns of the grid were hidden
- Fix unexpected behavior which prevented the lightbox and inline editors from overriding constraint dates

### 6.1.6

- Fix issue with not working click handlers of QuickInfo popup after a second gantt.init call
- Fix issue with QuickInfo popup not showing up if show_chart config is set to false
- Fix incorrect `action` argument for dataProcessor router after vertical drag-and-drop
- Fix issue when gantt.createTask ignores the `index` parameter

### 6.1.5

- Fix script error on a second gantt.init call when show_chart config is disabled
- Fix incorrect position of order_branch placeholder in the marker mode

### 6.1.4

- Fix script error on reinitialization of gantt in the IE browser
- Fix incorrect behavior of Tooltip extension when gantt.destructor is called
- Fix incorrect work of inline editors in keyboard_navigation_cell mode when grid contains hidden columns
- Fix bug in the Undo extension when Redo action for recreation of new tasks did not restore all properties
- Fix regression in GPL build which caused a script error on a second gantt.init call

### 6.1.3

- gantt.createTask/gantt.addTask should use root_id config value instead of hardcoded 0 id
- Performance increase for worktime calculations for minute and hour duration units
- Minor performance increase for rendering large lists of tasks in the smart rendering mode
- Ensure vertical drag-and-drop doesn't start when the user selects text inside an inline editor
- Fix script error from keyboard navigation in the cell mode after deleting last tasks from the chart
- Ensure Gantt cleans up autogenerated static background style elements after destruction or reinitialization
- Ensure inline editors are not active when read-only mode is enabled
- Fix incorrect selection of grid header cells in the cell mode of keyboard navigation when the sort config is enabled
- Fix regression in the auto_types config which prevented auto type change when new tasks are added
- Fix bug when returning false from onTaskDblClick blocked onLinkDblClick as well
- Fix script error when parsing constraint dates from JSON data
- Fix incorrect position of tasks and markers with the skip_off_time config
- Fix incorrect height of markers after reordering tasks via drag and drop
- New tasks receive the initial value of the progress property
- Fix incorrect task position after vertical drag and drop in the marker mode
- Fix script error from gantt.destructor when the resource panel is enabled
- Fix the bug which caused an empty line to be displayed in a typeselect block
- Fix the bug which caused a task not to be recognized as a part of critical path after id change

### 6.1.2

- Keyboard navigation: add a method for getting the active cell
- Fix incorrect work of the resource panel after creating a new datastore to overwrite the previous one
- Fix incorrect values of query parameters in the POST mode of dataProcessor
- Fix incorrect result of gantt.getClosestWorkTime when called without specifying a direction
- Fix issue when the English locale couldn't override the previously added locale
- Fix script error with gantt.undo and indent actions in the grid
- Fix SalesForce compatibility: new resize listener was broken in SF, fallback is added

### 6.1.1

- Add missing locale options for the resource lightbox control
- Fix script error when using gantt.destructor together with the dataProcessor
- Fix script error when using gantt.destructor together with the resource panel
- Fix the filesize of the tooltip extension
- Fix unexpected call of the onTaskDblClick event while double clicking on a link element
- Fix stuck lightbox cover if gantt.init is called while lightbox is opened
- Fix issues with lightbox and the tooltip extension in the full-screen mode

### 6.1.0

- Ability to add an overlay for the Gantt Chart (PRO)
- Time constraints for tasks (PRO)
- Routing options for dataProcessor
- Project-level working calendars (PRO)
- Ability to create tooltips for all the elements of dhtmlxGantt
- Ability to import dhtmlxGantt as an ES6 module

### 6.0.7

- reduce the number of redundant repaints of the resource diagram
- fix script error from the resource diagram after deleting a task
- fix script error from the fullscreen extension after exiting fullscreen mode on the `Esc` key
- fix incorrect state of links drag and drop when dragging a link between multiple charts on the page. Creating links between gantts is not supported
- fix script error after deleting multiple selected tasks using keyboard navigation extension
- fix default mapping of inline editors. Inline editors shouldn't block keyboard shortcuts on task cells

### 6.0.4

- fix incorrect task position after task vertical dnd in order_branch='marker' mode
- fix script error after deleting a sub-tree which contains selected task
- fix script error on Save/Cancel lightbox containing resource filters

### 6.0.2

- Fix referenceError: getResourceAssignments is not defined when importing Gantt into Vue.js project
- Fix script error on deleting task after assigning resource to it via resource form
- Fix JS error in resource diagram after second initialization of Gantt
- Fix script error on toggle timeline visibility when marker extension is used
- Fix page freeze on gantt.parse if tasks tree contains cyclic references, script error is thrown instead

### 6.0

- Advanced resource management
- New lightbox control for resource management
- Resource histogram
- Add ability to group by multiple resources
- Updated branch ordering
- Public methods for total slack and free slack
- Add JSON-REST dataprocessor mode
- Import from Excel added to online service
- Auto resize when container size changes
- Performance update for auto_types
- Performance update for auto scheduling

### 5.2

- Inline editing in grid
- Split task support
- Updated keyboard navigation
- Add checkbox and radio controls to the lightbox
- Add ability to set task types automatically
- Add ability to use a placeholder row for creating new tasks
- Auto Scheduling performance improvements
- New methods and events for Auto scheduling and Undo extension
- Updated Content Security Policy extension
- Various bugfixes

### 5.1

- Resource load diagram
- RTL mode
- Horizontal scroll for grid and other layout improvements
- Destructors for gantt and data processor instances
- Ability to set min/max widths of grid columns
- Updated API events for a multiselect extension
- Ability to drag and drop projects
- Fixed issues with keyboard navigation in smart rendering mode
- Many bugfixes

### 5.0

- Major architecture overhaul
- Added global layout config
- Added material skin
- Various bugfixes

### 4.2

- Work Time calendars at the task and resource levels
- WBS code (outline numbers) calculation
- Autoscroll for drag and drop operations
- Persian (Farsi) locale
- The getter function for key navigation shortcuts
- The config for cascade deleting of nested tasks and links
- The ability to scroll timeline horizontally on Shift+a mouse wheel movement
- German and Italian locales are updated
- GIF images in the Gantt skins are replaced with PNG
- various fixes

### 4.1

- Added keyboard navigation
- Added WAI-ARIA support
- Added High-contrast themes
- Updated Auto Scheduling and Critical Path calculations (PRO version)
- Performance improvements for worktime calculation and timescale rendering
- Croatian locale added
- Turkish locale updated
- Fixed bug redrawing vertical markers using gantt.updateMarker
- Fixed bug with gantt.showTask error in smart rendering mode
- Bugfixes for skip_off_time config and multi-tier scales configurations
- Bugfixes with dataProcessor and REST mode support

### 4.0

- Added Smart rendering of big data sets feature
- Added Undo/Redo feature
- Public API improvements - public helpers for popups, ajax, environment variables
- Public API cleanup - remove redundant global objects, resolve conflicts with dhtmlxSuite
- Updated critical path calculation - add support for lag/lead of links
- Updated Spanish and Chinese locales
- Minor bugfixes

### 3.3

- Added dependency Auto Scheduling feature *
- Added support for Fullscreen mode
- Added support of unscheduled tasks
- Added initial support of Content Security Policy
- Allow specifying per column grid sorting settings
- Improved branch ordering feature - allow D'n'D between levels
- Support of REST mode for ajax loading/saving
- Support of backward planning

* The marked functionality requires Commercial or Enterprise license, and not provided under GPL

### 3.2

- Added ability to group tasks by custom properties
- Added multiple selection
- Added export to iCal and to Excel
- Added public events for managing tasks reordering in a grid
- Added ability to specify time range in year selector
- Major performance improvement of worktime and critical path calculations
- New samples and API events

### 3.1

- Added ability to drag tasks on touch devices
- Incorrect tooltip behavior on expand/collapse task tree fixed
- Order of API events during gantt initialization fixed
- Issues with markers and multiple initialization of the gantt fixed
- Issues with markers and gantt.clearAll fixed
- Issues with gantt.serialize method and nested projects of gantt tree fixed
- Fixes in French locale
- Improvements in time range calculation

### 3.0

- Support of Baselines, Deadlines and other custom elements of the timeline *
- Critical path support *

- Ability to display vertical lines in a timeline area (Today line, Status line, etc.)

- Ability to resize Grid by D'n'D, ability to hide/show columns dynamically *
- Simplified API for coloring tasks and links *
- New performance-related options - dynamic loading and simple background rendering *

- Extended configuration for managing 'readonly' state of the tasks
- Extended set of methods for managing task tree hierarchy

- Support of task types and ability to skip time from the scale was removed from a Free version of the component

* The marked functionality requires Commercial or Enterprise license, and not provided under GPL


### 2.1

- Milestone and Projects support
- Custom configuration of the lightbox for different task types
- Non-linear scales, ability to skip time from the scale

- Ability to calculate duration in work days/hours instead of calendar time

- Support of multiple gantts on the page (requires PRO version)

- Updated some localisations
- Added more configurations and API methods events
- Various bugfixes

### 2.0

- jQuery integration
- Major performance improvements
- Ready-to-use PHP integration

- Configurable multi-line scales
- Configurable multi-column grid with optional sorting and Drag-n-Drop
- Configurable popup form for editing tasks
- All text elements can be defined through templates
- All date strings can be configured
- All text labels can be localized

- Default skin changed to "terrace"
- 3 new skins
- Bars can have an optional inner resizer
- Optional UI for task creation
- Vertical and horizontal lines can be colored based on custom rules

- Loading and serialization from JSON
- Loading and serialization with the simplified XML format
- 3 types of task linking
- Gantt charts work on touch devices

- A LOT of events added
- Templates and configuration options added
- API simplified, it uses a single gantt object instead of a bunch of different objects