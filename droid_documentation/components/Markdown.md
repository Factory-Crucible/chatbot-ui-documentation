
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format respectively. These components are integral to the project as they provide the functionality to display markdown content and code snippets in a readable and user-friendly manner.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component named `MemoizedReactMarkdown`. The component uses the `react-markdown` library to render markdown content and optimizes performance by preventing unnecessary re-renders through memoization.
- `CodeBlock.tsx`: This TypeScript component file exports a functional component named `CodeBlock`. The component is used to display code blocks in markdown format, with syntax highlighting provided by the `react-syntax-highlighter` library. It also includes functionality to copy the code to the clipboard and download the code as a file.

### Key Components

The `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx` files are the key components in this directory. 

- `MemoizedReactMarkdown.tsx` is crucial as it provides the functionality to render markdown content within the chatbot UI. By using React's `memo` function, it optimizes performance by preventing unnecessary re-renders, ensuring that the chatbot UI remains responsive and efficient.
- `CodeBlock.tsx` is equally important as it provides the functionality to display code blocks in markdown format. This is particularly useful when the chatbot needs to display code snippets to the user. The component also includes additional features such as syntax highlighting, copying code to the clipboard, and downloading code as a file, enhancing the user experience.

### Usage & Examples

The components in this directory are used throughout the codebase wherever markdown content or code blocks need to be displayed. 

For instance, the `MemoizedReactMarkdown` component could be used to render markdown content received from an API. The component would be used as follows:

```typescript
<MemoizedReactMarkdown>{markdownContent}</MemoizedReactMarkdown>
```

The `CodeBlock` component could be used within the `MemoizedReactMarkdown` component to display code blocks. The usage would look something like this:

```typescript
<CodeBlock language={language} value={code}/>
```

Please note that these examples are illustrative and may not represent the exact usage within the codebase.
