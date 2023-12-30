
## components/Markdown

The `components/Markdown` directory houses two TypeScript components, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`. These components are responsible for rendering markdown content and displaying code blocks in markdown format respectively. The `MemoizedReactMarkdown.tsx` component optimizes performance by preventing unnecessary re-renders, while the `CodeBlock.tsx` component provides syntax highlighting and functionality to copy code to clipboard and download code as a file.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component named `MemoizedReactMarkdown`. The component uses the `react-markdown` library to render markdown content and optimizes performance by preventing unnecessary re-renders.
- `CodeBlock.tsx`: This TypeScript component file exports a functional component named `CodeBlock`. The component is used to display code blocks in markdown format, provides syntax highlighting, and offers functionality to copy code to clipboard and download code as a file.

### Key Components

- `MemoizedReactMarkdown.tsx`: This component is crucial as it renders markdown content in the application. It uses memoization to optimize performance by preventing unnecessary re-renders, which is particularly beneficial in scenarios where the markdown content does not change between renders.
- `CodeBlock.tsx`: This component is responsible for displaying code blocks in markdown format. It uses `react-syntax-highlighter` for syntax highlighting, enhancing readability of code. Additionally, it provides functionality to copy code to clipboard and download code as a file, improving user experience.

### Usage & Examples

The `MemoizedReactMarkdown.tsx` component is used to render markdown content in the application. It is a memoized component, meaning it only re-renders when the markdown content changes. This is beneficial in scenarios where the markdown content remains static between renders, as it prevents unnecessary re-rendering and optimizes performance.

The `CodeBlock.tsx` component is used to display code blocks in markdown format. It provides syntax highlighting using `react-syntax-highlighter`, which enhances the readability of the code. The component also provides functionality to copy the code to clipboard and download the code as a file, offering a better user experience.
