
## Markdown Component Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot-ui project. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, each serving a unique purpose in the markdown rendering process. These components are integral to the project as they provide the functionality to display markdown content and code blocks in a user-friendly and efficient manner.

### Contents

The `components/Markdown` directory is composed of two TypeScript files:

- `MemoizedReactMarkdown.tsx`: This file exports a memoized functional component that uses the `react-markdown` library to render markdown content. The component is optimized for performance by preventing unnecessary re-renders through memoization.

- `CodeBlock.tsx`: This file exports a functional component that displays code blocks in markdown format. It uses `react-syntax-highlighter` for syntax highlighting and provides functionality to copy the code to clipboard and download the code as a file.

There are no subdirectories within this directory.

### Key Components

The `components/Markdown` directory houses two critical components:

- `MemoizedReactMarkdown`: This component is crucial for rendering markdown content within the chatbot-ui project. It uses the `react-markdown` library to convert markdown syntax into HTML, allowing for the display of rich text content. The component is memoized using React's `memo` function, which optimizes performance by preventing unnecessary re-renders when the markdown content remains unchanged.

- `CodeBlock`: This component is responsible for displaying code blocks within markdown content. It uses the `react-syntax-highlighter` library to provide syntax highlighting, enhancing readability of the code. The component also offers functionality to copy the code to clipboard and download the code as a file, enhancing user experience.

### Usage & Examples

The `MemoizedReactMarkdown` and `CodeBlock` components are used throughout the chatbot-ui project wherever markdown content needs to be displayed. 

For instance, `MemoizedReactMarkdown` might be used to render user-generated markdown content in a chat message or to display markdown-formatted documentation within the application. The component is used by passing the markdown content as children:

```typescript
<MemoizedReactMarkdown>{markdownContent}</MemoizedReactMarkdown>
```

The `CodeBlock` component is used within the `MemoizedReactMarkdown` component to render code blocks. It takes two props: `language` and `value`. `language` is the programming language of the code block, and `value` is the actual code to be displayed. An example usage might look like this:

```typescript
<CodeBlock language="javascript" value="console.log('Hello, world!');" />
```

These components are integral to the project's ability to display rich, interactive content and provide a user-friendly interface for the chatbot.
