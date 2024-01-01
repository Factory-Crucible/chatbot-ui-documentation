
## **tests** Directory

The `__tests__` directory is a dedicated space for testing in this project. It is structured to mirror the main codebase, allowing for a clear and organized testing structure. The directory contains a subdirectory named `utils`, which serves as a testing suite for the application's utility functions. Within `utils`, there's another subdirectory named `app`. The `app` subdirectory contains a test file named `importExports.test.ts`. This file is responsible for validating the import and export operations of the application. It ensures that the objects being exported conform to the expected format for each version. Additionally, it tests a function named `cleanData`, which is designed to update data from older export formats to the latest one. The test verifies that the updated data aligns with the expected structure of the current format.

### Contents

The `__tests__` directory contains the following subdirectories and files:

- `utils`: This subdirectory serves as a testing suite for the application's utility functions. It contains a subdirectory named `app`, which houses a test file `importExports.test.ts` that validates the functionality of import and export operations.
- `utils/app`: This subdirectory contains test files for the application's utility functions. Specifically, it includes a file named `importExports.test.ts` which tests utility functions related to import and export operations in the application.
- `utils/app/importExports.test.ts`: This is a test file for utility functions related to import and export operations in the application. It imports several functions and types from the application's utility and types directories.

### Key Components

- `importExports.test.ts`: This file is a critical component of the testing suite. It tests the import and export operations of the application, ensuring that the objects being exported conform to the expected format for each version. It also tests the `cleanData` function, which is designed to update data from older export formats to the latest one.

### Usage & Examples

The `__tests__` directory is used to house all the test files and suites for the application. The structure of this directory mirrors the main codebase, allowing for an organized and intuitive testing structure. For example, the `utils/app/importExports.test.ts` file tests the utility functions related to import and export operations in the application. It verifies different versions of the export format, ensuring that a given object matches the expected format for each version. The file also tests the `cleanData` function, which converts data from older export formats to the latest one, and checks that the cleaned data aligns with the expected structure of the latest format.
