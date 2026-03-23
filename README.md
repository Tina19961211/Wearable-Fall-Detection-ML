🧠 Wearable Fall Detection using Machine Learning
Detecting dangerous falls using wearable sensor data and deep learning
Falls are one of the leading causes of injury and hospitalization among older adults worldwide. Early detection of a fall — or even the transition toward a fall — can dramatically reduce response time and prevent severe complications.
This project explores how wearable accelerometer data and machine learning can detect fall events in real time, enabling future smart health monitoring systems for vulnerable populations.
The goal is to demonstrate how health analytics and wearable technologies can work together to improve patient safety and independence.
 
🏥 Why This Problem Matters
Every year:
•	1 in 4 adults over age 65 experiences a fall
•	Falls are the leading cause of injury-related deaths among older adults
•	Many falls occur when individuals are alone, delaying medical response
Wearable technologies — such as smart watches and sensor-based monitoring systems — provide a powerful opportunity to detect falls automatically and immediately.
This project explores how machine learning models trained on wearable sensor data can identify:
•	normal daily activity
•	unstable motion that precedes a fall
•	actual fall events
The long-term vision is continuous health monitoring through wearable devices that can alert caregivers, clinicians, or emergency services.
 
📊 Dataset
This study uses the SISFall Dataset, a widely used dataset for fall detection research.
The dataset contains wearable inertial sensor data collected during simulated daily activities and fall events.
Each sample represents a time window of accelerometer measurements from wearable sensors.
Event Classes
The dataset defines three motion states:
Non-Fall (Normal Activity)
Activities of daily living such as walking, sitting, and standing.
Pre-Impact Fall (Alert Stage)
A transition period where the individual moves from a stable state toward a dangerous posture.
Fall Event
A sudden motion leading to a loss of balance and impact.
In this project, the model learns to distinguish normal movement from fall-related motion patterns.
 
🧪 Methods
The analysis pipeline consists of several stages commonly used in health data science and wearable signal processing.
1️⃣ Data Processing
Wearable sensor signals were structured into 512-length time windows, representing short motion sequences.
These windows capture temporal movement patterns that precede and occur during falls.
 
2️⃣ Deep Learning Model
A Convolutional Neural Network (CNN) was trained to detect fall patterns within time-series sensor data.
CNNs are particularly effective for wearable signals because they can identify:
•	rapid acceleration spikes
•	abnormal motion transitions
•	characteristic fall signatures
The model architecture includes:
•	1D Convolution layers
•	pooling layers
•	fully connected classification layers
This allows the network to automatically learn motion features directly from raw sensor data.
 
3️⃣ Model Training
The dataset was divided into:
•	training set
•	validation set
•	test set
Training involved optimizing classification performance while minimizing overfitting.
Performance was evaluated using:
•	precision
•	recall
•	F1 score
•	confusion matrix
•	ROC curves
These metrics are especially important in healthcare AI, where false negatives and false positives have different consequences.
 
📈 Results
The trained model demonstrated strong performance in detecting fall-related motion patterns.
Test Set Performance
Metric	Score
Accuracy	97.6%
Precision	0.99
Recall	0.97
F1 Score	0.98
Confusion Matrix
	Predicted Non-Fall	Predicted Fall
Actual Non-Fall	36,752	1,016
Actual Fall	342	18,542
The model successfully identifies most fall events while maintaining high accuracy during normal activity.
This balance is crucial for wearable health systems, since excessive false alarms could reduce user trust.
 
🧠 What This Means for Digital Health
The results suggest that machine learning models trained on wearable sensor data can reliably detect fall events.
Such systems could eventually support:
•	remote patient monitoring
•	elderly care technologies
•	fall alert systems in smart homes
•	rehabilitation monitoring
•	hospital fall prevention systems
With further development, wearable AI systems could enable continuous passive health monitoring that improves safety without limiting independence.
 
🔬 Future Work
Several directions could further improve real-world wearable fall detection systems:
•	distinguishing pre-fall instability from actual falls
•	combining multiple sensors (accelerometer + gyroscope)
•	reducing model size for real-time wearable deployment
•	integrating explainable AI for clinical interpretation
These improvements would move the system closer to practical clinical or consumer wearable applications.
 
🛠 Technologies Used
Python
TensorFlow / Keras
NumPy / Pandas
Scikit-Learn
Matplotlib
 
👩‍🔬 About the Author
Tina Eskandari
PhD Student: Physical Therapy
Research focus:
•	rehabilitation science
•	wearable technologies
•	digital health analytics
•	machine learning for clinical applications
Her research explores how computational tools can improve rehabilitation outcomes and patient monitoring.
