🧩 Drag and Drop Activity

An interactive assessment component designed for matching exercises and knowledge verification. This activity allows users to categorize or assign topics to specific scenarios using intuitive drag-and-drop mechanics.

🚀 Live Demo

Explore the Drag and Drop Activity Component Here

✨ Project Overview

The Drag and Drop Activity provides a hands-on way for learners to apply their knowledge. By physically moving "Topic Bank" items into designated "Drop Zones," users engage in active learning and receive immediate corrective feedback.

Key Features

Interactive Matching: Users can grab items from a sidebar bank and drop them into corresponding scenario cards.

Immediate Validation: * Correct Match: The drop zone turns Midnight Blue, displays the topic text, and hides the original item from the bank.

Incorrect Match: The zone briefly flashes red with a "Try Again" message, resetting itself for another attempt.

Real-time Feedback: Uses a dynamic feedback-overlay system that injects status messages directly into the UI upon interaction.

Completion State: A success message automatically appears once all four matches are correctly identified.

Responsive Sidebar: On desktop, the layout uses a two-column grid (1.5fr 1fr); on mobile, it stacks vertically for optimal touch targets.

🛠️ Technical Implementation

HTML5 Drag and Drop API: Built using native browser events (dragstart, dragover, dragleave, drop) for high performance and low overhead.

Data Transfer: Utilizes e.dataTransfer.setData() to pass unique IDs between the dragged element and the target drop zone.

Dynamic Styling: * Uses Tailwind CSS for layout and spacing.

Custom CSS handles complex states like .dragging (lowers opacity) and .drag-over (highlights potential drop targets).

Feedback System: The handleMatch and handleError functions manage the visual state of the application, ensuring that the matchesFound counter accurately triggers the final completion message.

📂 Design Tokens

Midnight Blue (#1f2a52): Used for the header and the "Correct" state of drop zones.

Teal (#00bec7): The primary color for draggable items and "drag-over" highlights.

Light Aqua (#d2f0f0): Used for the initial state of drop zones and card borders.

Slate Grey (#abb5bf): Used for the "Topic Bank" dashed border and the reset button.

📖 Usage Instructions

To customize the activity, edit the scenarios-container and the topic-bank. Ensure that the data-target attribute on the drop-zone matches the id of the corresponding draggable-item:

<!-- The Target Zone -->
<div class="drop-zone" data-target="topic_id">Drop Here</div>

<!-- The Matching Item -->
<div class="draggable-item" draggable="true" id="topic_id">Topic Label</div>


📄 License

MIT License - Developed as part of the accounts-eles UI component library.
