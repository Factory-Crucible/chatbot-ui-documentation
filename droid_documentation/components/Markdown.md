
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown content within the chatbot user interface. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format, respectively. These components are integral to the project as they enhance the user experience by providing a visually appealing and efficient way to display markdown content and code snippets.

### Contents

The `components/Markdown` directory is a straightforward structure with no subdirectories. It contains two TypeScript files:

- `MemoizedReactMarkdown.tsx`: This file exports a memoized functional component that uses the 'react-markdown' library to render markdown content. It optimizes performance by preventing unnecessary re-renders.

- `CodeBlock.tsx`: This file exports a functional component that displays code blocks in markdown format. It uses 'react-syntax-highlighter' for syntax highlighting and provides functionality to copy the code to clipboard and download the code as a file.

### Key Components

The `components/Markdown` directory houses two critical components that contribute to the functionality and performance of the chatbot user interface:

- `MemoizedReactMarkdown`: This component is crucial for rendering markdown content in the chatbot UI. It uses the 'react-markdown' library to convert markdown into HTML. To optimize performance and prevent unnecessary re-renders, the component is memoized using React's 'memo' function.

- `CodeBlock`: This component is responsible for displaying code blocks in markdown format. It enhances the user experience by providing syntax highlighting using 'react-syntax-highlighter' and offering options to copy the code to clipboard and download the code as a file. The component also uses 'next-i18next' for internationalization, ensuring that the chatbot UI is accessible to users of different languages.

### Usage & Examples

The components in the `components/Markdown` directory are used throughout the codebase wherever markdown content or code blocks need to be displayed. 

For instance, the `MemoizedReactMarkdown` component could be used in a chat message component to render markdown content received from the chatbot. Here's a simplified example of how it might be used:

```typescript
import { MemoizedReactMarkdown } from '../components/Markdown/MemoizedReactMarkdown';

function ChatMessage({ content }) {
  return (
    <div className="chat-message">
      <MemoizedReactMarkdown>{content}</MemoizedReactMarkdown>
    </div>
  );
}
```

Similarly, the `CodeBlock` component could be used within the `MemoizedReactMarkdown` component to render code blocks in markdown content. Here's a simplified example:

```typescript
import { CodeBlock } from '../components/Markdown/CodeBlock';

function CodeSnippet({ language, code }) {
  return (
    <div className="code-snippet">
      <CodeBlock language={language} value={code} />
    </div>
  );
}
```

These examples are illustrative and may not represent the exact usage in the codebase. Always refer to the actual code for precise implementation details.
