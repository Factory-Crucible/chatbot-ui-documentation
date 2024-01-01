
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format respectively. These components are integral to the project as they enhance the user experience by providing a visually appealing and efficient way to display markdown content and code blocks.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component named `MemoizedReactMarkdown`. It utilizes the `react-markdown` library to render markdown content and optimizes performance by preventing unnecessary re-renders.
- `CodeBlock.tsx`: This TypeScript component file exports a functional component named `CodeBlock`. It is responsible for displaying code blocks in markdown format. It uses the `react-syntax-highlighter` for syntax highlighting and provides functionality to copy the code to clipboard and download the code as a file.

### Key Components

The `components/Markdown` directory houses two key components:

- `MemoizedReactMarkdown`: This component is crucial as it handles the rendering of markdown content within the chatbot UI. It is memoized to optimize performance by preventing unnecessary re-renders, ensuring a smooth and efficient user experience.
- `CodeBlock`: This component is responsible for displaying code blocks in markdown format. It enhances the user experience by providing syntax highlighting and options to copy the code to clipboard and download the code as a file. The file name for download is generated using a utility function, ensuring a unique name for each download.

### Usage & Examples

The components within the `components/Markdown` directory are used throughout the codebase wherever markdown content or code blocks need to be displayed. 

For instance, the `MemoizedReactMarkdown` component could be used to render markdown content received from an API. It would be used as follows:

```typescript
<MemoizedReactMarkdown>{apiResponse.markdownContent}</MemoizedReactMarkdown>
```

The `CodeBlock` component could be used to display a code block within a markdown content. It would be used as follows:

```typescript
<CodeBlock language={codeBlock.language} value={codeBlock.value} />
```

In this example, `codeBlock.language` would be the programming language of the code block and `codeBlock.value` would be the actual code to be displayed.
