The source code used to generate the models is L2C_1.ipynb.

The final model submitted for the demo is L2C_1.h5 with an onnx file for use with PiCar Simulator.

Records of development and implementation results can be found below.

**LAB DEMO COMPETITION EXPERIMENTAL RESULTS:**
- Perfect score of 100 on all 3 levels of track in the PiCar simulator
- Perfect score on the real world track (completed full lap with no errors)
<img width="328" height="209" alt="image" src="https://github.com/user-attachments/assets/a4f1d49b-6aed-4e68-ae32-55fba7bb008c" />

- Score and class ranking not yet released

**IMPLEMENTATION & VALIDATION**
- By lab 5 the dense neural network was able to follow simple lines consistently
- By lab 6 with the final model, it was able to follow more complex curves, as seen in the demo video
- For the physical car testing, please see the video at https://www.youtube.com/watch?v=JUabfKyiU3c  

- The PiCar simulator results were very promising, with our personal testing on custom tracks resulting in 100 score on all levels of difficulty
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/0b0e4430-2bc1-4b0d-8bf3-d0aa04bd8342" />
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/eb2e9f1b-a8b9-49d1-a201-549ddd9fd2c2" />
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/93b97134-4bac-4fec-aa0f-4fcad7ffbeb0" />

- This success extended to demo day with our model getting 100 score on all tracks
<img width="584" height="381" alt="image" src="https://github.com/user-attachments/assets/ed3c5593-2d88-4aa2-8789-93402c485f04" />

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
<img width="589" height="462" alt="image" src="https://github.com/user-attachments/assets/45478e3b-1dde-4f13-a75a-a774f8481daf" />
<img width="819" height="602" alt="image" src="https://github.com/user-attachments/assets/1e41c797-f255-475c-ba04-05cdbf9ffa3d" />

