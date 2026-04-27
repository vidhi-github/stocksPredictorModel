# 📈 Stock Price Prediction using ARIMA, LSTM & Hybrid Models

This project explores stock price forecasting by combining traditional statistical methods and modern deep learning techniques. It demonstrates how ARIMA, LSTM, and a Hybrid ARIMA-LSTM model can be used to capture different patterns in financial time series data and improve prediction accuracy.

##🔍 Modeling Approaches
📘 ARIMA (AutoRegressive Integrated Moving Average)
A statistical time series model used for forecasting based on past values and errors.
Works well for linear patterns and short-term predictions.
Requires stationary data, achieved through differencing and transformation.
Hyperparameters (p, d, q) selected using techniques like AIC, MINIC, and ESACF.
⚠️ Limitation: Struggles with non-linear trends and market volatility.

##🤖 LSTM (Long Short-Term Memory)
A type of Recurrent Neural Network (RNN) designed to learn long-term dependencies.
Effective in capturing non-linear patterns, trends, and temporal dependencies in stock data.
Uses sliding window sequences and normalized inputs (MinMaxScaler).
Built with multiple LSTM layers, dropout (to prevent overfitting), and dense output layers.
Optimized using Adam optimizer and Mean Squared Error (MSE) loss.
✅ Strength: Handles complex and volatile market behavior better than traditional models.

##🔗 Hybrid ARIMA-LSTM Model
Combines the strengths of both approaches:
ARIMA models the linear components of the time series.
LSTM captures the residual non-linear patterns left by ARIMA.

#Workflow:
Apply ARIMA to model and remove linear trends.
Pass ARIMA residuals to LSTM for learning non-linear patterns.
Combine outputs for final prediction.
✅ Advantage: Improves overall accuracy by leveraging both statistical and deep learning insights.
🚀 Particularly useful for financial data with mixed linear and non-linear characteristics.

##📊 Key Insight
ARIMA → Best for simple, linear, short-term forecasting
LSTM → Best for complex, non-linear, long-term dependencies
Hybrid Model → Best overall performance by combining both worlds

##🌐 Deployment

The models are integrated into a Streamlit web application, allowing users to:

Select stocks dynamically
Visualize predictions
Compare ARIMA, LSTM, and Hybrid outputs interactively

#### 🌐 Live Demo
Check out the deployed web app: [Stock Price Predictor](https://stockpredictsp500.streamlit.app/)
