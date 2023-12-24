
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot user interface. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format, respectively. These components are integral to the project as they enhance the user experience by providing a visually appealing and efficient way to display markdown content and code snippets.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component named 'MemoizedReactMarkdown'. It uses the 'react-markdown' library to render markdown content and optimizes performance by preventing unnecessary re-renders.
- `CodeBlock.tsx`: This TypeScript component file exports a functional component named 'CodeBlock'. It is used to display code blocks in markdown format, with syntax highlighting provided by 'react-syntax-highlighter'. It also includes functionality to copy the code to clipboard and download the code as a file.

### Key Components

The `components/Markdown` directory houses two key components:

- `MemoizedReactMarkdown`: This component is crucial for rendering markdown content within the chatbot UI. It uses the 'react-markdown' library to convert markdown syntax into HTML, providing a rich text format for the chatbot's responses. The component is memoized using React's 'memo' function, which optimizes performance by preventing unnecessary re-renders when the markdown content remains unchanged.
- `CodeBlock`: This component is responsible for displaying code blocks in markdown format. It enhances the user experience by providing syntax highlighting for code snippets, making them easier to read and understand. The component also includes functionality to copy the code to clipboard and download the code as a file, providing users with easy access to the code snippets.

### Usage & Examples

The components in the `components/Markdown` directory are used throughout the chatbot UI to render markdown content and display code blocks.

For instance, the `MemoizedReactMarkdown` component might be used to render a chatbot response that includes markdown syntax. The component would take the markdown content as a prop and convert it into HTML, providing a rich text format for the response.

```tsx
<MemoizedReactMarkdown>{markdownContent}</MemoizedReactMarkdown>
```

The `CodeBlock` component might be used to display a code snippet within a chatbot response. The component would take the programming language and the code snippet as props, and display the code with syntax highlighting.

```tsx
<CodeBlock language="javascript" value={codeSnippet} />
```

These examples represent typical usage patterns for the components in the `components/Markdown` directory. However, the actual usage may vary depending on the specific requirements of the chatbot UI.
