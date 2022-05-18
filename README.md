# LSTM_ventilation
Model that uses time-series vital sign data to predict need for ventilation. The benefit of this tool is it uses only routinely collect observational features and no lab results. This means it can use data collected from nurse visits.

Current results are AUC of 0.81. This outperforms a static NN (AUC 0.76) that uses only latest vital sign measurement. I believe this can be improved with some fine-tuning that will come in due time:

![image](https://user-images.githubusercontent.com/43360672/169157085-037429fd-dc80-4739-8ac5-73b9170cf7cc.png)

Predictions are also very well calibrated (wuth marginal over-estimation in high risk patients being more beneficial)

![image](https://user-images.githubusercontent.com/43360672/169157230-fb9d3961-bcc4-4bd8-815f-7c5e0681a162.png)



