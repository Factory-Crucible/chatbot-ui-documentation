
## components/Markdown

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format respectively. These components are integral to the project as they enhance the user experience by providing a visually appealing and efficient way to display markdown content and code snippets.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component named `MemoizedReactMarkdown`. The component uses the `react-markdown` library to render markdown content and optimizes performance by preventing unnecessary re-renders.
- `CodeBlock.tsx`: This TypeScript component file exports a functional component named `CodeBlock`. The component is used to display code blocks in markdown format, with syntax highlighting provided by `react-syntax-highlighter`. It also includes functionality to copy the code to clipboard and download the code as a file.

### Key Components

The `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx` files are the key components in this directory. 

- `MemoizedReactMarkdown.tsx` is crucial as it handles the rendering of markdown content within the chatbot UI. It uses the `react-markdown` library to convert markdown syntax into HTML, providing a rich text format for the chatbot's responses. The component is memoized using React's `memo` function, optimizing performance by preventing unnecessary re-renders when the markdown content remains unchanged.
- `CodeBlock.tsx` is responsible for displaying code blocks in markdown format. It enhances the user experience by providing syntax highlighting for code snippets, making them easier to read and understand. The component also includes functionality to copy the code to clipboard and download the code as a file, providing users with convenient ways to reuse the code snippets.

### Usage & Examples

The components in this directory are used throughout the chatbot UI to render markdown content and display code blocks.

For instance, the `MemoizedReactMarkdown` component could be used to render a chatbot's response that includes markdown syntax. The component would take the response as a prop and convert the markdown syntax into HTML, providing a rich text format for the response.

The `CodeBlock` component could be used to display a code snippet in a chatbot's response. The component would take the programming language and the code snippet as props, and display the code snippet with syntax highlighting. It would also provide options to copy the code to clipboard and download the code as a file.

Please note that these are hypothetical examples and the actual usage of these components may vary depending on the specific requirements of the chatbot UI.
