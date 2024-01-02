# Tree of Thoughts: A LMQL Implementation

Tree of Thoughts is a powerful implementation of Language Model Query Language (LMQL), designed to simulate a tree-like thought process. It applies a natural selection process to guide reasoning and constrain results, making it a versatile tool for problem-solving.

## Key Features

Tree of Thoughts is designed to be as customizable as possible, allowing each tree instance to be configured to solve a specific problem. It can also apply a callback function to the result, providing flexibility in output format. Here are some of its main features:

- **Asynchronous:** Supports asynchronous operations for improved performance.
- **Configurable:** Allows extensive customization to suit specific use cases.
- **Result Validation:** Supports both prompt-based and programmatic result validation.

## Upcoming Features

We're constantly working to improve Tree of Thoughts. Here are some features we plan to add:

- **Multiple Arguments and Argument Types:** Enhance the flexibility of input.
- **Feature Weighting:** Assign relative importance to selection criteria.
- **Dynamic Width:** Determine the number of branches that should stem from each thought dynamically.

## How It Works

Tree of Thoughts operates in iterations, each consisting of a review phase, a generation phase, and an evaluation phase:

- **Selection:** Selects the top-k scoring lines of thought.
- **Review:** Checks if the selected lines of thought contain an answer.
- **Generation:** Generates a fixed number of branching thoughts from selected leaf thoughts. If a selected leaf contains an answer, a conclusion is generated instead.
- **Evaluation:** Scores new thoughts against defined criteria to determine the relative strength of the threads. If any conclusions were generated, they are validated and returned if they pass.

## Usage

To get started with Tree of Thoughts, check out the `examples` folder. In a nutshell, there are three configurations: one for the initial prompt, one that governs the reasoning dynamics (evaluation, answer recognition), and one that describes how answer attempts are handled (conclusion generation, callbacks, validation).

Stay tuned for more detailed usage instructions and examples!