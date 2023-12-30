
## components/Spinner

The `components/Spinner` directory is dedicated to the Spinner component, a React component that displays a spinning animation typically used to indicate a loading state. The directory contains two files: `Spinner.tsx` and `index.ts`. The `Spinner.tsx` file defines the Spinner component, while the `index.ts` file serves as an entry point for the Spinner component, simplifying imports elsewhere in the project.

### Contents

The `components/Spinner` directory contains the following files:

- `Spinner.tsx`: This file defines the Spinner component. The component accepts 'size' and 'className' as optional props, with 'size' controlling the spinner's dimensions and 'className' allowing for additional CSS classes. The spinner is created using SVG and includes an animation for the spinning effect.
- `index.ts`: This file serves as an entry point for the Spinner component, exporting the default export from 'Spinner.tsx'. This setup simplifies imports elsewhere in the project, as the Spinner component can be imported directly from 'components/Spinner' without specifying the 'Spinner.tsx' file.

### Key Components

The key component in this directory is the Spinner component, defined in the `Spinner.tsx` file. This component is used throughout the project to indicate a loading state in the user interface. It is a reusable component that can be customized with different sizes and additional CSS classes.

### Usage & Examples

The Spinner component is used in various parts of the codebase where a loading state needs to be indicated. It can be imported directly from 'components/Spinner' thanks to the `index.ts` file.

Example of usage:

```typescript
import Spinner from 'components/Spinner';

// In a component
return (
  <div>
    Loading data...
    <Spinner size="2em" className="text-blue-500" />
  </div>
);
```

In this example, the Spinner component is used to indicate that data is loading. The size of the spinner is set to '2em', and a 'text-blue-500' CSS class is applied to it.
