
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format, respectively. These components are integral to the chatbot UI's ability to display rich text content and code snippets, enhancing the user experience and providing a more interactive and informative interface.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component named `MemoizedReactMarkdown`. It uses the `react-markdown` library to render markdown content and optimizes performance by preventing unnecessary re-renders through memoization.

- `CodeBlock.tsx`: This TypeScript component file exports a functional component named `CodeBlock`. It is used to display code blocks in markdown format, with syntax highlighting provided by `react-syntax-highlighter`. It also includes functionality to copy the code to the clipboard and download the code as a file.

### Key Components

The `components/Markdown` directory houses two key components that play a significant role in the chatbot UI's markdown rendering capabilities:

- `MemoizedReactMarkdown`: This component is responsible for rendering markdown content within the chatbot UI. It uses the `react-markdown` library to convert markdown syntax into HTML, providing a rich text experience for the user. The component is memoized using React's `memo` function, which optimizes performance by preventing unnecessary re-renders unless the markdown content changes.

- `CodeBlock`: This component is used to display code blocks within the markdown content. It takes two props: `language` and `value`, which represent the programming language of the code block and the actual code to be displayed, respectively. The component uses `react-syntax-highlighter` for syntax highlighting, enhancing readability of the code. It also provides functionality to copy the code to the clipboard and download the code as a file, offering a user-friendly way to interact with code snippets.

### Usage & Examples

The components within the `components/Markdown` directory are used throughout the chatbot UI to render markdown content and display code blocks.

For instance, the `MemoizedReactMarkdown` component might be used in a chat message component to render markdown content received from the chatbot. It would be used like so:

```tsx
<MemoizedReactMarkdown>{chatMessage.content}</MemoizedReactMarkdown>
```

The `CodeBlock` component, on the other hand, would be used within the `MemoizedReactMarkdown` component to render code blocks within the markdown content. It would be used like so:

```tsx
<CodeBlock language={codeBlock.language} value={codeBlock.value} />
```

These examples demonstrate typical usage patterns of the components within the `components/Markdown` directory, highlighting their role in enhancing the chatbot UI's markdown rendering capabilities.
