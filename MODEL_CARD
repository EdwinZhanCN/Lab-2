# Model Card: Activity Recognition GRU

## Intended Use
Real-time prediction for basic human activities (Walking, Walking Up, Walking Down, Sitting, Standing, Laying) using smartphone inertial sensors like accelerometer and gyroscope.

## Non-Intended Use
This model is not suitable for any clinical analysis, fall detection for the elderly, or diagnosing motor impairments. Moreover, it is not calibrated for complex activity recognition like Swimming, Dancing, etc.

## 3. Evaluation Protocol
This model is evaluated strictly on a subject-disjoint split. The test sets are entirely unseen during both the training and tuning phases.

We use Macro-F1 score and per-class accuracy via a confusion matrix as our metrics.

## 4. Known Failure Modes
The model struggles to distinguish static postures like "Sitting" and "Standing". Because the both postures yield a relatively static gravity vector. Minor shifts in phone orientation can blur the boundary between those two classes.

## 5. Privacy & Ethics Note
- Continuous tracking of IMU data could leak sensitive user information. In a real deployment, inference should strictly run *on-device* without transmitting raw sensor data to the external media.
* Ethics: The dataset only includes adults aged  from 19 to 48. The model may exhibit bias for children, the elderly, or users with disabilities.
