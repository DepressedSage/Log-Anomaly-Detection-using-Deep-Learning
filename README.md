# Log-Anomaly-Detection-using-Deep-Learning

This project combines the power of the Drain algorithm for log parsing with Long Short-Term Memory (LSTM) neural networks for anomaly detection in system logs. The Drain algorithm preprocesses and compiles system logs into structured event templates, which are then used as input for an LSTM-based model. The model detects anomalies in the system execution and reports them to the root user or system administrator.

### Introduction

This project focuses on building an efficient system for detecting anomalies in system logs using a two-step process: 

1. **Drain Log Parsing**: We employ the Drain algorithm, a fixed-depth tree-based online log parsing method. This algorithm preprocesses raw log messages using domain-specific regular expressions, compiles them into event templates, and structures them in a parse tree for efficient searching.

2. **LSTM-based Anomaly Detection**: The preprocessed and structured log data is then used as input to an LSTM-based deep learning model. LSTMs are designed to capture long-term dependencies in sequential data, making them suitable for time series analysis and anomaly detection.

### Getting Started

To get started with this project, follow these steps:

1. Clone this repository:

   ```sh
   git clone https://github.com/DepressedSage/Log-Anomaly-Detection-using-Deep-Learning.git
   ```

2. Navigate to the project directory:

   ```sh
   cd Log-Anomaly-Detection-using-Deep-Learning
   ```

3. Install the required dependencies (see [Prerequisites](#prerequisites)).

4. Run the code using your preferred Python environment.

### Prerequisites

Before running the code, ensure you have the following dependencies installed:

- Python >= 3.6
- NumPy
- Pandas
- Keras
- TensorFlow

You can install these dependencies using the following command:

```sh
pip install numpy pandas keras tensorflow
```

### Usage

The workflow of this project can be summarized as follows:

1. **Drain Log Parsing**:
   - Raw log messages are preprocessed using domain-specific regular expressions to remove variable components.
   - The preprocessed messages are then matched against a parse tree based on log message length and token similarity.
   - Log groups are formed in the parse tree, representing similar log events.

2. **LSTM-based Anomaly Detection**:
   - The structured log data (event templates) are used as input for the LSTM model.
   - The LSTM model is trained on normal system behavior, learning the patterns within the log data.
   - During inference, the model predicts whether a new log sequence is anomalous based on the learned patterns.

### Project Structure and Flow
![image](https://github.com/DepressedSage/Log-Anomaly-Detection-using-Deep-Learning/assets/78322027/874ca136-9d83-4c92-b5b9-5ff8defee0af)



### Code Overview

The project is organized into several sections:

- Drain Log Parsing:
  - Preprocessing raw log messages using domain-specific regular expressions.
  - Building and traversing a parse tree based on log message length and token similarity.
  - Creating and updating log groups in the parse tree.

- LSTM-based Anomaly Detection:
  - Defining the architecture of the LSTM model.
  - Preprocessing the structured log data for LSTM input.
  - Training the LSTM model on normal log sequences.
  - Detecting anomalies using the trained LSTM model.

### Results

The results of this project are observed through the anomalies detected by the LSTM-based model. Anomalies indicate deviations from the learned patterns of normal system behavior. The accuracy, precision, recall, and F1-score of the model can be used to evaluate its performance.

### Contributing

Contributions to this project are welcome. If you find any issues or want to add enhancements, feel free to submit a pull request.

### License

This project is licensed under the [MIT License](LICENSE).

For more details on the Drain algorithm and LSTM-based anomaly detection, please refer to the respective research papers and documentation.
