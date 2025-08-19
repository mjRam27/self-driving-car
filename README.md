
# 🏎️ Self-Driving Car Project  

This project implements a **behavioral cloning model** for a self-driving car using deep learning.  
The model is trained on driving simulator data (images + steering angles) and learns to predict steering commands directly from camera images.  

---

## 📌 Features  

### 🔹 Data preprocessing & balancing
- Binned steering angle distribution to avoid bias toward straight driving.  
- Cropped images to remove sky/hood and focus on road.  
- Normalized inputs for stable training.  

### 🔹 Data augmentation (to simulate real-world conditions)
- ✅ **Panning** → simulates car drifting left/right.  
- ✅ **Zooming** → simulates objects being closer/further.  
- ✅ **Brightness adjustment** → simulates day/night/shadows.  
- ✅ **Flipping** → balances left/right turns.  

### 🔹 Model training
- Implemented in **Jupyter Notebook** (`Self_driving_car.ipynb`).  
- CNN inspired by the **NVIDIA architecture**.  
- Input size: `66x200x3` (YUV images).  
- Output: predicted steering angle.  

### 🔹 Deployment
- `drive.py` connects to the **Udacity Self-Driving Car Simulator** via socket.  
- Uses trained model (`model/model.h5`) to predict steering in real-time.  


## ⚙️ Installation  

1️⃣ Clone this repo  
git clone https://github.com/mjRam27/self-driving-car.git
cd self-driving-car

2️⃣ Install dependencies

pip install -r requirement.txt

3️⃣ Set up simulator
Download and install the [Udacity Self-Driving Car Simulator](https://github.com/udacity/self-driving-car-sim).


## 🚀 Running the trained model in simulator

Since a trained model (`model/model.h5`) is already included, you can directly test it without retraining:
Run:
python drive.py


Steps:

1. Start the simulator.
2. Select **Autonomous Mode**.
3. The car will drive on its own 🚗💨, using predictions from `model/model.h5`.
*(Simulator = road 🌍, Model = brain 🧠, Camera = eyes 👀, Steering = hands on the wheel ✋)*

---

## 🔮 Future Improvements

* Lane detection + multi-camera input.
* Predict throttle & brake in addition to steering.
* Train on real-world driving datasets.

---

## 🙌 Acknowledgements

* [Udacity Self-Driving Car Simulator](https://github.com/udacity/self-driving-car-sim)

