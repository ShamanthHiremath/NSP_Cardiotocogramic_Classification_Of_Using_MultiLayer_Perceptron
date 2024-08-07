# NSP_Cardiotocogramic_Classification_Of_Using_MultiLayer_Perceptron

# Fetal Health Classification using Cardiotocography (CTG) Data

## Overview

During pregnancy, acquiring direct information about the fetus is challenging. Obstetricians often rely on indirect information, with one of the most important indicators being the fetal heart rate (FHR). Cardiotocography (CTG) is a commonly used method to monitor fetal well-being by recording the fetal heart rate and uterine activity.

This project aims to classify fetal health based on CTG data using a neural network built with TensorFlow. The model utilizes a three-layer neural network with the Adam optimizer and categorical classification as the loss function. The achieved accuracy is 87.229%.

## Dataset

The dataset used in this project contains various features related to fetal heart rate and uterine activity. The accepted parameters for the fetus are as follows (all values are in beats per minute):

- Baseline fetal heart rate between 110 and 160.
- Baseline variance larger than 5.

## Cardiotocography (CTG)

Cardiotocography (CTG) is an investigative method used to observe fetal well-being by recording:

1. Instant fetal heart rate (FHR)
2. Uterine activity (UC)

The information obtained from CTG is used for early identification of pathological states such as inherited heart deficiencies, fetal suffering, or hypoxia. Early diagnosis and intervention can prevent permanent harm or even death of the fetus.

## Neural Network Model

The neural network model used in this project is built using the TensorFlow library. The model structure includes:

1. Input Layer
2. Two Hidden Layers
3. Output Layer

The model is optimized using Adam's algorithm and employs categorical classification for loss calculation.

### Model Architecture

- **Input Layer:** 21 features
- **Hidden Layer 1:** Dense layer with 8 units and ReLU activation
- **Hidden Layer 2:** Dense layer with 50 units and ReLU activation
- **Output Layer:** Dense layer with 3 units and Softmax activation

### Training

The model is trained using the following parameters:
- **Optimizer:** Adam
- **Loss Function:** Categorical Crossentropy
- **Epochs:** 200
- **Batch Size:** 32
- **Validation Split:** 0.2

### Evaluation

The model is evaluated on a test dataset, achieving an accuracy of 87.229%.

## Usage

To use this project, follow these steps:

1. Clone the repository:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. Install the required dependencies:
    ```bash
    pip install tensorflow keras numpy pandas
    ```

3. Run the model training script:
    ```bash
    python train_model.py
    ```

4. Evaluate the model and make predictions on new data:
    ```python
    # Load your new data
    new_data = [132, 0.006514658, 0, 0.008143322, 0, 0, 0, 16, 2.4, 0, 19.9, 117, 53, 170, 9, 0, 137, 136, 138, 11, 1]
    
    # Normalize the data (assuming a normalize function is defined)
    new_data = normalize(new_data)
    
    # Predict the class
    predicted_class = model.predict(new_data)
    print(predicted_class)
    ```

## References

1. Reference 1
2. Reference 2
3. Reference 3
4. Reference 4
5. Reference 5

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

