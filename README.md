# Chatbot UI Documentation Droid Demo

## About

This repository is designed to showcase the Documentation Droid. Within the repository, there is a new folder called [droid_documentation](./droid_documentation/).
This folder is generated automatically when a repository receives a Documentation Droid.

## How It Works
When you first onboard to the factory platform - we generate a knowledge backend called HyperCode. HyperCode contains a functional layer (Code Graph & Metadata) and a knowledge layer (Multi-Resolution Hierarchal Semantic Map). We use HyperCode in every Droid to enable enhanced codebase reasoning that is always up to date and goes beyond fine-tuned models and standard retrieval based methods.

The Documentation Droid navigates HyperCode, and then builds out a structure for your documentation which reflects things like the volume of content, the directory structure, important entry files, and metadata around how your codebase was built. The documentation files then are produced to allow anybody to understand and navigate the codebase, with example usage patterns and explanations included.

There is a 1-1 mapping of every file in your codebase to your documentation. When changes are made to the files which warrant an update to your documentation, the Documentation Droid will create a pull request to reflect those changes. This works when there's a single file refactored, and when there's 100 files refactored.

You can also update the documentation the Documentation Droid generates - and the Droid will keep those changes in mind when updating the files. That way, you can ensure your docs always maintain the information, look, and feel that you'd prefer.

## Personalization

We work with customers to personalize the Documentation Droid to reflect their preferences. To start, the Documentation Droid's outputs reflect a general documentation strategy focused on onboarding new developers. But there may be use cases, information, or patterns for your documentation that you'd like to see reflected. 

As you work with Factory, we can help customize the Droids to ensure maximum value to you. 

## Credits

Chatbot UI is an open source chat UI for AI models. [Original source](https://github.com/mckaywrigley/chatbot-ui)