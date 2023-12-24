
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format, respectively. These components are integral to the chatbot UI's ability to display rich text content and code snippets, enhancing the user experience and providing a more interactive and engaging interface.

### Contents

The `components/Markdown` directory is composed of two TypeScript files:

- `MemoizedReactMarkdown.tsx`: This file exports a memoized functional component that uses the `react-markdown` library to render markdown content. The component is optimized for performance by preventing unnecessary re-renders using React's `memo` function.

- `CodeBlock.tsx`: This file exports a functional component that displays code blocks in markdown format. It uses `react-syntax-highlighter` for syntax highlighting and provides functionality to copy the code to clipboard and download the code as a file.

There are no subdirectories within the `components/Markdown` directory.

### Key Components

The `components/Markdown` directory houses two key TypeScript components:

- `MemoizedReactMarkdown`: This component is crucial for rendering markdown content within the chatbot UI. By using the `react-markdown` library, it enables the display of rich text content. The component is memoized to optimize performance by preventing unnecessary re-renders, ensuring a smooth and responsive user experience.

- `CodeBlock`: This component is responsible for displaying code blocks in markdown format. It enhances the chatbot UI's functionality by allowing users to view code snippets in a clear and highlighted format. The component also provides the ability to copy the code to clipboard and download the code as a file, adding to the interactive nature of the chatbot UI.

### Usage & Examples

The components within the `components/Markdown` directory are used throughout the chatbot UI to render markdown content and display code blocks.

For instance, the `MemoizedReactMarkdown` component might be used to render user-generated markdown content in a chat message. It would take the markdown content as a prop and render it into HTML, providing a rich text display.

```typescript
<MemoizedReactMarkdown>{userMessage}</MemoizedReactMarkdown>
```

The `CodeBlock` component could be used to display a code snippet within a chat message. It would take the programming language and the code snippet as props, and display the code in a highlighted format.

```typescript
<CodeBlock language="javascript" value={codeSnippet} />
```

These examples represent typical usage patterns for the components within the `components/Markdown` directory. They illustrate how these components contribute to the functionality and interactivity of the chatbot UI.
