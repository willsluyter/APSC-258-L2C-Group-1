The source code used to generate the models is L2C_1.ipynb.

The final model submitted for the demo is L2C_1.h5 with an onnx file for use with PiCar Simulator.

Records of development and implementation results can be found below.

**LAB DEMO COMPETITION EXPERIMENTAL RESULTS:**
- Perfect score of 100 on all 3 levels of track in the PiCar simulator
- Perfect score on the real world track (completed full lap with no errors)
(image of demo)
- Score and class ranking not yet released

**IMPLEMENTATION**

**DEVELOPMENT PROGRESS**

Below is a summary of what we did in each lab.

Lab 1 - Environment & Python Setup

- Installed and configured the Python environment with Anaconda
- Set up Jupyter Notebook, Spyder, and google colab for running code

Lab 2 — PiCar Connection & Control Testing

- Connected to the PiCar via Wi-Fi and verified communication through the controller interface
- Installed required dependencies and tested simple manual motor control using Python commands
- Confirmed proper functionality of steering and throttle via socket-based control

Lab 3 — Simulation & Dataset Collection

- Installed and configured the PiCar Simulator environment
- Designed custom tracks to generate diverse driving scenarios
- Collected labeled image data with corresponding steering angles, adjusting capture rates to emphasize turning behavior
- Exported and prepared the dataset for training
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b19421ab-46a4-426d-9a67-15f68d26c1dc" />

Lab 4 — Data Exploration & Baseline Model

- Uploaded dataset to Google Colab and visualized image samples and steering distributions
- Identified dataset imbalances and ensured adequate representation of turning cases
- Trained a baseline linear regression model and evaluated performance using error metrics (MSE, MAE, RMSE)
- Exported the model to ONNX format for simulator testing
<img width="785" height="498" alt="image" src="https://github.com/user-attachments/assets/06a3de2b-961b-4a7e-858d-0d4ff8200f45" />

Lab 5 — Dense Neural Network Development

- Built and trained a dense neural network using Keras
- Experimented with network architecture (layers, neurons, and structure) to reduce validation loss
- Compared performance against the baseline model
- Deployed models to both simulator (ONNX) and physical PiCar (.h5) for testing
<img width="622" height="454" alt="image" src="https://github.com/user-attachments/assets/e3517855-bcb0-4a73-b29e-9fa44e865e13" />

Lab 6 — CNN Optimization & Final Model

- Upgraded the model to a convolutional neural network (CNN) using Conv2D, MaxPooling, and Dense layers
- Tuned hyperparameters such as filter size, number of layers, and learning rate
- Evaluated regularization techniques (e.g., Dropout) and selected the best-performing configuration
- Achieved significantly improved performance in simulation and real-world testing, with reliable autonomous track following.

