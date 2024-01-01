
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format respectively. These components are integral to the project as they enhance the user interface by providing a rich text format and syntax-highlighted code blocks.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component named `MemoizedReactMarkdown` that uses the `react-markdown` library to render markdown content. The component is memoized to optimize performance by preventing unnecessary re-renders.
- `CodeBlock.tsx`: This TypeScript component file exports a functional component named `CodeBlock` that displays code blocks in markdown format. It uses `react-syntax-highlighter` for syntax highlighting and provides functionality to copy the code to clipboard and download the code as a file.

### Key Components

The `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx` files are the key components in this directory. 

`MemoizedReactMarkdown.tsx` is crucial as it renders markdown content within the chatbot UI. By memoizing this component, the application optimizes performance by avoiding unnecessary re-renders, thus enhancing the user experience.

`CodeBlock.tsx` is another vital component that enhances the user interface by displaying syntax-highlighted code blocks in markdown format. It also provides additional functionality such as copying code to clipboard and downloading code as a file, making it easier for users to interact with code snippets.

### Usage & Examples

The `MemoizedReactMarkdown` component is used throughout the codebase wherever markdown content needs to be rendered. It takes markdown content as a prop and renders it into HTML. 

The `CodeBlock` component is used within the `MemoizedReactMarkdown` component to render code blocks in markdown content. It takes two props: 'language' and 'value'. 'language' is the programming language of the code block and 'value' is the actual code to be displayed.

```typescript
// Usage of MemoizedReactMarkdown
<MemoizedReactMarkdown>{markdownContent}</MemoizedReactMarkdown>

// Usage of CodeBlock within MemoizedReactMarkdown
<MemoizedReactMarkdown
  components={{
    code({node, inline, className, children, ...props}) {
      const match = /language-(\w+)/.exec(className || '')
      return !inline && match
        ? <CodeBlock language={match[1]} value={String(children).replace(/\n$/, '')} {...props} />
        : <code className={className} {...props}>{children}</code>
    }
  }}
>
  {markdownContent}
</MemoizedReactMarkdown>
```
