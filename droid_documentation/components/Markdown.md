
## components/Markdown

The `components/Markdown` directory houses two TypeScript components, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`. These components are responsible for rendering markdown content and displaying code blocks in markdown format, respectively. They are integral to the representation of markdown content and code snippets within the chatbot UI.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component named `MemoizedReactMarkdown`. The component uses the `react-markdown` library to render markdown content and optimizes performance by preventing unnecessary re-renders.
- `CodeBlock.tsx`: This TypeScript component file exports a functional component named `CodeBlock`. The component is used to display code blocks in markdown format, with syntax highlighting provided by `react-syntax-highlighter`. It also includes functionality to copy the code to clipboard and download the code as a file.

### Key Components

- `MemoizedReactMarkdown`: This component is crucial for rendering markdown content within the chatbot UI. It uses the `react-markdown` library and optimizes performance by memoizing the component to prevent unnecessary re-renders.
- `CodeBlock`: This component is responsible for displaying code blocks in markdown format. It uses `react-syntax-highlighter` for syntax highlighting and provides functionality to copy the code to clipboard and download the code as a file.

### Usage & Examples

The `MemoizedReactMarkdown` component is used to render markdown content within the chatbot UI. It is memoized using React's `memo` function to optimize performance by preventing unnecessary re-renders. The memoization comparison function checks if the `children` prop, which presumably contains the markdown content, has changed between renders.

The `CodeBlock` component is used to display code blocks in markdown format. It takes two props: `language` and `value`. `language` is the programming language of the code block and `value` is the actual code to be displayed. The component provides functionality to copy the code to clipboard and download the code as a file. The file name for download is generated using a utility function `generateRandomString`.
