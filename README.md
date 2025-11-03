# Bank-Note-Authentication-using-Random-Forest

📘 Overview

This project predicts whether a banknote is genuine or fake using Machine Learning.
The model is trained with the Random Forest Classifier algorithm on a dataset containing statistical features extracted from banknote images — such as variance, skewness, curtosis, and entropy.

A Streamlit web app is created to provide an easy-to-use interface for real-time prediction.

🚀 Features

✅ Built using Random Forest Classifier

🧠 Takes 4 input features: Variance, Skewness, Curtosis, and Entropy

💻 Interactive Streamlit-based web interface

📊 Displays real-time prediction results

🗂️ Trained and deployed using a saved model (classifier.pkl)

| Component                | Technology                             |
| ------------------------ | -------------------------------------- |
| **Programming Language** | Python                                 |
| **ML Framework**         | scikit-learn                           |
| **Web Framework**        | Streamlit                              |
| **Model Serialization**  | pickle                                 |
| **Libraries Used**       | pandas, numpy, PIL, sklearn, streamlit |

Project Structure
BankNote_Authentication/
│
├── app.py                    # Streamlit web app
├── classifier.pkl            # Trained Random Forest model
├── BankNote_Authentication.ipynb  # Jupyter notebook (training and model creation)
├── requirements.txt          # Python dependencies
└── README.md                 # Project documentation

⚙️ How It Works

Dataset:
The dataset includes image statistics of banknotes with 4 key features:

Variance of Wavelet Transformed image

Skewness of Wavelet Transformed image

Curtosis of Wavelet Transformed image

Entropy of image

Model Training:
A Random Forest Classifier is trained using these features to classify notes as:

0 → Fake Note

1 → Genuine Note

Model Deployment:
The trained model is saved as classifier.pkl using the pickle library and deployed via Streamlit.
🧠 Model Details

Algorithm: Random Forest Classifier

Accuracy: ~99% (on test data)

Reason for Choosing Random Forest:

Handles feature importance well

Reduces overfitting

Provides stable and high accuracy

🖼️ Streamlit Interface

The web app allows users to input the following values:
| Feature  | Description                       |
| -------- | --------------------------------- |
| Variance | Measures data spread in the image |
| Skewness | Measures image asymmetry          |
| Curtosis | Measures peakedness or flatness   |
| Entropy  | Measures randomness or noise      |

noise

👉 Once the user enters all 4 values and clicks Predict, the app displays:
“The output is [0 or 1]” → Fake or Real Note

🧾 Example Output

Input Example:
| Variance | Skewness | Curtosis | Entropy |
| -------- | -------- | -------- | ------- |
| 2.3      | 6.7      | -1.2     | 0.4     |

Predicted Output: ✅ Genuine Bank Note
