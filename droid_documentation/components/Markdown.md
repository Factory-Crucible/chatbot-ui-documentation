
## components/Markdown Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format respectively. These components are integral to the chatbot UI as they enable the display of markdown content and code snippets in a user-friendly and efficient manner.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript file exports a memoized functional component named `MemoizedReactMarkdown`. The component uses the `react-markdown` library to render markdown content and optimizes performance by preventing unnecessary re-renders through memoization.

- `CodeBlock.tsx`: This TypeScript file exports a functional component named `CodeBlock`. The component is used to display code blocks in markdown format, with syntax highlighting provided by `react-syntax-highlighter`. It also offers functionality to copy the code to clipboard and download the code as a file.

### Key Components

The `components/Markdown` directory houses two key components:

- `MemoizedReactMarkdown`: This component is crucial for rendering markdown content within the chatbot UI. By using React's `memo` function, it ensures that the markdown content is only re-rendered when necessary, thereby optimizing performance.

- `CodeBlock`: This component is responsible for displaying code blocks within the chatbot UI. It enhances the user experience by providing syntax highlighting and options to copy the code to clipboard or download it as a file. The component's internationalization support, provided by `next-i18next`, ensures that the UI is accessible to users from different locales.

### Usage & Examples

The `MemoizedReactMarkdown` and `CodeBlock` components are used throughout the chatbot UI to render markdown content and display code blocks respectively. For instance, when the chatbot needs to display a message containing markdown content, it would use the `MemoizedReactMarkdown` component. Similarly, when a code snippet needs to be displayed within the chatbot UI, the `CodeBlock` component would be used.

Here's a simplified example of how these components might be used:

```typescript
import { MemoizedReactMarkdown, CodeBlock } from './components/Markdown';

// To render markdown content
<MemoizedReactMarkdown>{markdownContent}</MemoizedReactMarkdown>

// To display a code block
<CodeBlock language={language} value={codeSnippet} />
```

Please note that these examples are simplified and the actual usage of these components may involve additional props and logic.
