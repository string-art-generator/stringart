


Welcome! You can generate your own string art creations online at: https://stringart.vip/

Feel free to submit your works via Pull Request (PR) to this repository and share your creations with the community!

# StringArt Generator
This site implements an automatic image-to-string-art conversion tool. After uploading an image, the system automatically processes, analyzes, and generates the string connection sequence, dynamically displays the string art effect on the canvas, and allows exporting or step-by-step demonstration of the process.

----

## 1. Main Functional Flow
- **Image Upload**: User selects an image, which is automatically loaded onto the page.
- **Image Processing**:
	- Center-cropped to a square
	- Grayscaled
	- Circular crop
- **Pin Calculation**: Pins are evenly distributed on the circumference, and their coordinates are calculated.
- **Line Precalculation**: All pixel points between every pair of pins are precalculated.
- **Main Algorithm (String Art Generation)**:
	- Iteratively selects the best line (the one that covers the area with the largest difference from the original image)
	- Updates the error image after each line
	- Records the sequence of lines
	- Draws in real time on the canvas
- **Result Output**:
	- Draws the final string art image
	- Outputs the line sequence (can be saved or pasted)
	- Supports "step-by-step drawing" and "previous/next step" operations
	- Provides example pin sequences

## 2. Tech Stack
- **Frontend**: HTML, Bootstrap, jQuery
- **Image Processing**: OpenCV.js (client-side image processing), NumJS (numerical computation)
- **Canvas**: Used for drawing images and string art
- **Interaction**: Native JS event listeners and button operations
