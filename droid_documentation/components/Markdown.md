
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format, respectively. These components are integral to the project as they enable the display of markdown content and code snippets in the chatbot UI, enhancing the user experience and facilitating the sharing of code snippets.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component that uses the `react-markdown` library to render markdown content. The component is optimized for performance by preventing unnecessary re-renders.
- `CodeBlock.tsx`: This TypeScript component file exports a functional component that displays code blocks in markdown format. It uses `react-syntax-highlighter` for syntax highlighting and provides functionality to copy the code to clipboard and download the code as a file.

### Key Components

The key components within the `components/Markdown` directory are the `MemoizedReactMarkdown` and `CodeBlock` components.

- `MemoizedReactMarkdown`: This component is crucial as it is responsible for rendering markdown content within the chatbot UI. It uses the `react-markdown` library and is memoized using React's `memo` function to optimize performance by preventing unnecessary re-renders.
- `CodeBlock`: This component is used to display code blocks in markdown format. It enhances the user experience by providing syntax highlighting using `react-syntax-highlighter` and offering functionality to copy the code to clipboard and download the code as a file.

### Usage & Examples

The `MemoizedReactMarkdown` and `CodeBlock` components are used within the chatbot UI to render markdown content and display code blocks, respectively.

For instance, the `MemoizedReactMarkdown` component might be used to render a markdown-formatted message from the chatbot. The component would take the markdown content as a prop and render it into HTML.

The `CodeBlock` component could be used to display a code snippet shared in the chat. The component would take the programming language and the code snippet as props, and display the code with appropriate syntax highlighting. It also provides the user with options to copy the code to clipboard or download it as a file.
