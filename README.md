# # Baby Cry Predictor (py documentation)

### Introduction
The Baby Cry Predictor is a machine learning-based application developed as part of a graduation project. The aim of the project is to automatically analyze and predict the emotional state of a baby based on their cries. By leveraging audio processing techniques and a trained model, the application provides real-time predictions that can assist parents and caregivers in understanding and responding to the needs of the baby. This documentation focuses on the deployment aspect of the project, covering the steps involved in setting up and running the application.

### Prerequisites
Before deploying the Baby Cry Predictor, we ensured that the following prerequisites are met
### Deployment Steps
We Followed the steps below to deploy the Baby Cry Predictor application:

1. We Downloaded the Code: Downloaded the provided code file, `baby_cry.py`, and saved it to a convenient location on our system.

2. Trained Model: We Placed the trained model file, named "BabyCry.pkl", in the same directory as the code file. This model file contained the trained Random Forest Classifier model that was previously saved using the `pickle` library and we accessed it with open and pickle.load which are elements in pickle Library .

3. Run the Application: We Opend a command prompt or terminal window, navigated to the directory where the code file is located, and run the following command:
   ```
   streamlit run baby_cry.py
   ```

   This command will start the application and display a local URL, usually `http://localhost:8501`. We Opend this URL in our web browser to access the Baby Cry Predictor interface.

4. Application Interface: The Baby Cry Predictor interface consists of a title, "Baby Cry Predictor," and a "Start" button. Click the "Start" button to initiate audio recording.

5. Audio Recording: Upon clicking the "Start" button, the application will start recording audio for 5 seconds. You can make a baby cry sound during this time. The application will display a "Recording..." message while recording is in progress.

6. Prediction: After the recording is complete, the application will display a "Finished recording" message. The recorded audio will be saved to a file named "recorded_audio.wav" in the same directory as the code file.

7. Prediction Result: The application will then process the recorded audio by extracting Mel-frequency cepstral coefficients (MFCCs) using the `librosa` library. The mean MFCC values are calculated from the extracted features.

8. Model Prediction: The trained model, loaded from the "BabyCry.pkl" file using the `pickle` library, is then used to predict the emotional state of the baby based on the mean MFCC values. The predicted emotional state is displayed in the application interface.

