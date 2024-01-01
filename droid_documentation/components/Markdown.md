
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format respectively. These components are integral to the project as they provide the functionality to display markdown content and code snippets in a user-friendly and efficient manner.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component named `MemoizedReactMarkdown`. The component uses the `react-markdown` library to render markdown content and optimizes performance by preventing unnecessary re-renders.
- `CodeBlock.tsx`: This TypeScript component file exports a functional component named `CodeBlock`. The component is used to display code blocks in markdown format, with syntax highlighting provided by `react-syntax-highlighter`. It also includes functionality to copy the code to clipboard and download the code as a file.

### Key Components

The `components/Markdown` directory houses two key components:

- `MemoizedReactMarkdown`: This component is crucial for rendering markdown content within the chatbot UI. It uses the `react-markdown` library to convert markdown syntax into HTML, providing a user-friendly way to display markdown content. The component is memoized using React's `memo` function, which optimizes performance by preventing unnecessary re-renders when the markdown content remains unchanged.
- `CodeBlock`: This component is responsible for displaying code blocks within the markdown content. It uses the `react-syntax-highlighter` library to provide syntax highlighting, enhancing readability of the code. The component also includes functionality to copy the code to clipboard and download the code as a file, providing additional utility for users.

### Usage & Examples

The components within the `components/Markdown` directory are used throughout the chatbot UI to render markdown content and display code blocks.

For instance, the `MemoizedReactMarkdown` component can be used to render markdown content from a chat message:

```tsx
<MemoizedReactMarkdown>{chatMessage.content}</MemoizedReactMarkdown>
```

The `CodeBlock` component can be used within the `MemoizedReactMarkdown` component to display code blocks:

```tsx
<MemoizedReactMarkdown
  components={{
    code: ({node, inline, className, children, ...props}) => {
      const match = /language-(\w+)/.exec(className || '')
      return !inline && match
        ? <CodeBlock language={match[1]} value={String(children).replace(/\n$/, '')} {...props} />
        : <code className={className} {...props} />
    }
  }}
>
  {chatMessage.content}
</MemoizedReactMarkdown>
```

In this example, the `CodeBlock` component is used to render code blocks within the markdown content, providing syntax highlighting and additional functionality for code snippets.
