```markdown
# Test Markdown App

## Description
Test Markdown App is a web application designed to convert Markdown content into HTML. Utilizing the powerful `marked.js` library, this application allows users to load Markdown content from attachments, convert it to HTML, and display the result in a styled output area. The application is enhanced with Bootstrap for responsive design and `highlight.js` for syntax highlighting, ensuring an aesthetically pleasing and user-friendly experience.

## Features
- **Markdown to HTML Conversion**: Seamlessly convert Markdown text into HTML format.
- **Attachment Support**: Load Markdown content from file attachments.
- **Responsive Design**: Built with Bootstrap to ensure compatibility across various devices.
- **Syntax Highlighting**: Integrated `highlight.js` for enhanced code readability.
- **Live Preview**: Instantly see the rendered HTML as you edit the Markdown content.

## Setup Instructions
To set up the Test Markdown App locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/24f2008913/test-markdown-app-20251017163340.git
   ```

2. **Navigate to the project directory**:
   ```bash
   cd test-markdown-app-20251017163340
   ```

3. **Open the `index.html` file** in your preferred web browser to view the application:
   ```bash
   open index.html  # macOS
   start index.html # Windows
   xdg-open index.html # Linux
   ```

4. **Dependencies**: Ensure you have an internet connection to load external libraries from CDN.

## Usage Guide
1. **Loading Markdown**: Click on the file input to select a Markdown file from your device.
2. **Editing Markdown**: You can edit the Markdown content directly in the provided text area.
3. **Viewing Output**: The converted HTML will be displayed in the `#markdown-output` div in real-time as you make changes.
4. **Styling**: The application uses Bootstrap for styling, ensuring a clean and modern user interface.

## Code Explanation
The application is structured as follows:

- **index.html**: The main HTML file that includes the layout and references to CSS and JavaScript libraries.
- **styles.css**: Custom styles to enhance the appearance of the application beyond Bootstrap's default styling.
- **script.js**: The main JavaScript file that handles:
  - Loading Markdown files.
  - Converting Markdown to HTML using `marked.js`.
  - Displaying the converted HTML in the designated output area.
  - Initializing `highlight.js` for syntax highlighting.

### Key Code Snippets
- **Markdown Conversion**:
  ```javascript
  const markdownInput = document.getElementById('markdown-input');
  const outputDiv = document.getElementById('markdown-output');

  markdownInput.addEventListener('input', () => {
      const markdownText = markdownInput.value;
      const htmlContent = marked(markdownText);
      outputDiv.innerHTML = htmlContent;
      hljs.highlightBlock(outputDiv);
  });
  ```

## License Information
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Live Demo
Check out the live demo of the Test Markdown App at: [Live Demo](https://24f2008913.github.io/test-markdown-app-20251017163340/)
```
