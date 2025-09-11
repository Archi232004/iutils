BeautyBook: A Dynamic Table Visualization Tool for Iterative Processes
Abstract
BeautyBook is a lightweight Python class designed to facilitate the dynamic visualization of tabular data within Jupyter and Google Colab environments. It provides a simple, API-driven interface for logging data points, such as performance metrics from a machine learning training loop, and rendering them in a highly-styled, continuously updated HTML table. The tool leverages IPython.display to offer an in-place, real-time logging experience, eliminating the need for manual data frame reconstruction or external file writes during iterative processes.

Features
Real-time Updates: The table is updated dynamically in the output cell without generating new output, preserving notebook cleanliness.

Automatic Indexing: Each logged entry is automatically assigned an index number.

Responsive Styling: Columns automatically adjust their width based on the content to ensure optimal readability.

Standalone Class: The functionality is encapsulated within a single, portable Python class for easy integration into any notebook.

Installation
BeautyBook is distributed as a single Python class. To use it, simply copy and paste the BeautyBook class definition into a code cell within your Jupyter or Colab notebook.

```pip install beautybook```

Usage
The workflow consists of two primary steps: initializing the table and logging data.

1. Initialization
Instantiate the BeautyBook class with the desired column headers. The table will be rendered immediately with the header row.

# Initialize the table with column headers for a training loop
book = BeautyBook("Epoch", "Train Loss", "Validation Loss", "Accuracy")


2. Logging Data
Use the log method to append new rows of data to the table. The table will automatically update with each call. Ensure the number of data points passed to log matches the number of columns you defined during initialization.

# Sample Usage within a training loop
for epoch in range(1, 11):
    # Simulate a process generating metrics
    train_loss = 0.9**epoch
    val_loss = 0.95**epoch + 0.05
    accuracy = 1 - val_loss
    
    # Log the metrics to a new row in the table
    book.log(epoch, f"{train_loss:.4f}", f"{val_loss:.4f}", f"{accuracy:.2%}")
    time.sleep(0.5) # Simulate a time-consuming step


Design and Implementation
The core functionality of BeautyBook relies on the IPython.display.HTML function, which allows for the rendering of rich HTML content directly within the notebook. To enable dynamic updates, each table instance is assigned a unique display_id using the uuid module. The display() function's update=True parameter ensures that subsequent calls to _render_table() modify the existing output rather than creating new ones. Column widths are dynamically calculated using the ch CSS unit, which is proportional to the width of the '0' character, providing a responsive layout that adapts to the length of the content.

License
This project is licensed under the MIT License - see the LICENSE.md file for details.

Citation
If you use BeautyBook in your work, please consider citing it using the following format:

Author, A. (2024). BeautyBook: A Dynamic Table Visualization Tool for Iterative Processes. [link to source]
