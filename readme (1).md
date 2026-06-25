# **Stock Price Prediction using Simple RNN and LSTM**

This project demonstrates the use of **Simple RNN** (Recurrent Neural Network) and **LSTM** (Long Short-Term Memory) models to predict stock prices. The models are trained to forecast stock prices for 1-day, 5-day, and 10-day periods using historical stock data. The project includes hyperparameter tuning through a **Random Search** approach to optimize the models' performance and find the best configuration.

## **Introduction**

The objective of this project is to predict stock prices using two types of recurrent neural networks (RNNs): Simple RNN and LSTM. Both models are capable of handling sequential data, making them suitable for time-series forecasting tasks such as predicting stock prices.

## **Setup and Installation**

To get started with this project, you'll need to have the following dependencies installed:

* Python 3.x

* TensorFlow 2.x

* NumPy

* Matplotlib

* Pandas

* Scikit-learn

You can install the necessary packages via `pip`:

pip install tensorflow numpy matplotlib pandas scikit-learn

## **Dataset**

The dataset used in this project contains historical stock prices, which include the following columns:

* Date

* Open price

* High price

* Low price

* Close price

* Volume

This data is preprocessed and transformed to create sequences for training both the Simple RNN and LSTM models.

## **Model Development**

This project includes the development of two different types of recurrent neural networks:

### **1\. Simple RNN Model**

The Simple RNN model is a basic form of recurrent neural network, used to capture temporal dependencies in time-series data. The model architecture includes:

* **Input Layer:** A time-series input of shape `(number_of_timesteps, 1)`.

* **RNN Layer:** A single RNN layer with a specified number of units to capture sequential patterns.

* **Dropout Layer:** A regularization layer to reduce overfitting.

* **Dense Layer:** The final output layer for stock price prediction.

### **2\. LSTM Model**

The LSTM model is a more advanced type of RNN designed to handle long-range dependencies and mitigate issues like vanishing gradients. The LSTM model architecture includes:

* **Input Layer:** A time-series input of shape `(number_of_timesteps, 1)`.

* **LSTM Layers:** Two stacked LSTM layers to capture both short-term and long-term dependencies in the data.

* **Dropout Layers:** Regularization layers to prevent overfitting.

* **Dense Layer:** The final output layer for stock price prediction.

### **Hyperparameters for Both Models:**

* **Units:** Number of neurons in the RNN or LSTM layers.

* **Dropout Rate:** The dropout regularization rate.

* **Optimizer:** The optimizer used for training (Adam or RMSProp).

* **Learning Rate:** The learning rate for the optimizer.

* **Batch Size:** The number of samples processed before updating the model.

## **Hyperparameter Tuning**

Hyperparameter tuning is performed using **Grid Search**, where different combinations of hyperparameters are sampled and tested. The parameters being tuned include:

* **Units:** Number of units in the RNN or LSTM layers.

* **Dropout Rate:** Dropout regularization rate.

* **Optimizer:** Optimizer used (Adam or RMSProp).

* **Learning Rate:** The learning rate for the optimizer.

* **Batch Size:** The batch size used during training.

The best hyperparameters are selected based on the validation loss during the tuning process.

## **Evaluation Metrics**

The model's performance is evaluated using the following metrics:

* **Mean Squared Error (MSE):** Measures the average squared difference between predicted and actual values.

* **Mean Absolute Error (MAE):** Measures the average magnitude of errors between predicted and actual values.

* **Root Mean Squared Error (RMSE):** Measures the square root of the average squared differences between predicted and actual values. RMSE penalizes larger errors more heavily than MAE.

### 

### **Model Comparison:**

* **LSTM:** The LSTM model shows better performance in terms of handling long-term dependencies and capturing sequential patterns.

* **Simple RNN:** The Simple RNN model works effectively for basic sequential data but is limited in handling complex temporal dependencies compared to LSTM.

**Usage**

\#\#\# How to Use

To explore the stock price prediction models:

1\. Clone the repository or download the \`.ipynb\` notebook.  
2\. Open the notebook in Jupyter Notebook, JupyterLab, or any compatible environment (e.g., VS Code).  
3\. Run the cells sequentially to:  
   \- Load and preprocess the data  
   \- Train both the Simple RNN and LSTM models  
   \- Evaluate and compare their performance  
   \- Visualize the predictions vs actual stock prices

Make sure the necessary libraries are installed using:

pip install tensorflow numpy matplotlib pandas scikit-learn

**Contributors:**  
Shubhi Garg
