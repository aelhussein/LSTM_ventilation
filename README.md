# LSTM_ventilation
Model that uses time-series vital sign data to predict need for ventilation. The benefit of this tool is it uses only routinely collect observational features and no lab results. This means it can use data collected from nurse visits. Timesteps are 48, 36, 24 and 12hrs prior to ventilation. Data for controls taken at the point of admission to ICU with respiratory disease.

Current results are AUC of 0.81. This outperforms a static NN (AUC 0.76) that uses only latest vital sign measurement. Results are shown across all timesteps. Unsurprisingly, the predictions get better over time

![image](https://user-images.githubusercontent.com/43360672/169167163-2229c5e0-8256-466a-9bf6-cf98c0f5083a.png)

Predictions are also very well calibrated (wuth marginal over-estimation in high risk patients being more beneficial)

![image](https://user-images.githubusercontent.com/43360672/169167171-d010be28-6793-450b-91b9-1ac0ea84eccc.png)

I believe this can be improved with some fine-tuning that will come in due time.
