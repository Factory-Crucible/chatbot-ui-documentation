
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format, respectively. These components are integral to the project as they enhance the user experience by providing a visually appealing and interactive way to display markdown content and code snippets.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component named `MemoizedReactMarkdown`. It uses the `react-markdown` library to render markdown content and optimizes performance by preventing unnecessary re-renders through memoization.

- `CodeBlock.tsx`: This TypeScript component file exports a functional component named `CodeBlock`. It is used to display code blocks in markdown format, with syntax highlighting provided by the `react-syntax-highlighter` library. It also offers functionality to copy the code to the clipboard and download the code as a file.

### Key Components

The `components/Markdown` directory houses two key components:

- `MemoizedReactMarkdown`: This component is crucial for rendering markdown content within the chatbot UI. It uses the `react-markdown` library to convert markdown syntax into HTML, providing a rich text format for the chatbot's responses. The component is memoized using React's `memo` function, which optimizes performance by preventing unnecessary re-renders unless the markdown content changes.

- `CodeBlock`: This component is responsible for displaying code blocks within the markdown content. It uses the `react-syntax-highlighter` library to provide syntax highlighting, enhancing readability for users. The component also includes functionality to copy the code to the clipboard and download the code as a file, providing a user-friendly way to interact with code snippets.

### Usage & Examples

The components within the `components/Markdown` directory are used throughout the chatbot UI to render markdown content and display code blocks.

For instance, the `MemoizedReactMarkdown` component might be used to render a chatbot response that includes markdown syntax. The component would take the markdown content as a prop and return a React element with the content rendered as HTML.

```typescript
<MemoizedReactMarkdown>{markdownContent}</MemoizedReactMarkdown>
```

The `CodeBlock` component could be used within the `MemoizedReactMarkdown` component to display code blocks. It would take the programming language and the code as props and return a React element with the code displayed in a syntax-highlighted block.

```typescript
<CodeBlock language="javascript" value={codeSnippet} />
```

These examples represent typical usage patterns for the components within the `components/Markdown` directory.
