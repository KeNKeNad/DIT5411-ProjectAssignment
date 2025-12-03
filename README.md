# DIT5411-ProjectAssignment
DIT5411-ProjectAssignment

Report:
https://vtcmca-my.sharepoint.com/:w:/g/personal/240263863_stu_vtc_edu_hk/ETcpnhSh031HpTRxAZFdmTsBQmo6xjOmAQbyEE_x_hnR8Q?e=HcPGP1
PDF:
https://vtcmca-my.sharepoint.com/:p:/g/personal/240263863_stu_vtc_edu_hk/EdoykPtYGmJFrHz9VHBtdUMB12RtoJb_tKNHylU_1wZRnA?e=IblPpv

# Hong Kong Grass Minimum Temperature Prediction (1980–2025)

This project implements a deep learning-based time series forecasting pipeline to predict **daily grass minimum temperature** in Hong Kong using historical data from 1980 to 2025. It evaluates and compares **RNN**, **LSTM**, and **BiLSTM** models.

---

## Project Structure
├── dataset/
│   └── daily_HKO_GMT_ALL.csv      # Raw daily temperature data
├── DIT5411-ProjectAssignment/
│   ├── raw_data.png               # Plot of original train/test temperature
│   ├── predictions_comparison.png # Model predictions vs actual
│   ├── model_results.md           # Final MAE & RMSE comparison
├── your_notebook.ipynb            # The main notebook file
└── README.md                      # This file

## Dataset Overview
Source: Hong Kong Observatory (HKO)
Period: 1980-01-01 to 2025-10-30
Target: Grass Minimum Temperature (°C)
Format: Daily readings with year, month, day, and temperature values

## Models Implemented
All models use 30-day input sequences (SEQ_LEN = 30)
Trained for 100 epochs with batch size 32
Best model checkpoints saved using ModelCheckpoint
RNN : 2 × SimpleRNN + Dense & Basic recurrent
LSTM : 2 × LSTM + Dropout + Dense & Handles long-term
BiLSTM : Bidirectional LSTM × 2 + Dropout + Dense & Future context

## Requirements
Python 3.8+
TensorFlow 2.x
NumPy, Pandas, Matplotlib, Scikit-learn