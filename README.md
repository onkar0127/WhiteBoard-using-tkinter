# WhiteBoard-using-tkinter
This repository contains a simple White Board application built using the tkinter library in Python. The application provides a virtual whiteboard where users can draw, write, and erase using various tools
# Whiteboard App

The Whiteboard App is a simple yet powerful drawing application built using Python and the Tkinter library. It provides a virtual whiteboard where users can draw, erase, and save their creations.

## Installation

To use the Whiteboard App, you'll need to have Python and the following libraries installed:

- `tkinter`
- `PIL` (Python Imaging Library)

You can install these dependencies using pip:

```
pip install tkinter pillow
```

## Usage

1. Run the `whiteBoard.py` script to launch the application.
2. Use the toolbar at the top to select the drawing tool (pen or eraser), adjust the brush size, and choose the color.
3. Click and drag the mouse on the canvas to draw or erase.
4. Click the "Save" button to save the drawing as a PNG file.
5. Click the "Clear" button to start a new drawing.

## API

The `WhiteboardApp` class provides the following methods:

- `create_toolbar()`: Constructs the toolbar with various buttons and controls.
- `choose_color()`: Opens a color picker dialog to select the drawing color.
- `set_tool(mode)`: Sets the current drawing mode (pen or eraser).
- `paint(event)`: Handles the drawing or erasing on the canvas based on the selected tool.
- `reset(event)`: Resets the drawing coordinates when the mouse is released.
- `save_drawing()`: Saves the current drawing to a PNG file.
- `clear_canvas()`: Clears the canvas and resets the drawing image.

## Contributing

If you find any issues or have suggestions for improvements, feel free to open a new issue or submit a pull request on the project's GitHub repository.

## License

This project is licensed under the [MIT License](LICENSE).

## Testing

To run the tests for the Whiteboard App, you can use the built-in Python testing framework. Create a new file named `test_whiteBoard.py` and add your test cases.

```python
import unittest
from whiteBoard import WhiteboardApp

class TestWhiteboardApp(unittest.TestCase):
    def setUp(self):
        self.root = tk.Tk()
        self.app = WhiteboardApp(self.root)

    def test_choose_color(self):
        self.app.choose_color()
        self.assertIsNotNone(self.app.color)

    # Add more test cases as needed
```

Run the tests using the following command:

```
python -m unittest test_whiteBoard
```
