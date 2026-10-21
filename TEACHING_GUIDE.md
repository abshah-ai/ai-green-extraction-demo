# A 12–15 minute live demonstration
Dr. Abdul Bari Shah · KBTU

Prepare: open the notebook in Colab and run it once before the lecture. The saved outputs also provide a fallback if the connection fails. No GPU is required.

## 1. Explain the data (2 minutes)
Say: “These are simulated experiments for a hypothetical plant. In a real project, we would first perform experiments and measure recovery. Here we already have known outcomes, so we can teach the model the relationship between conditions and recovery.”

Explain that 70% ethanol means ethanol concentration in the initial ethanol–water solvent, not ethanol percentage in the extract. Four inputs are required, including solvent-to-solid ratio.

## 2. Split and train (3 minutes)
Say: “We let the model learn from 240 rows and keep 60 rows hidden. A Random Forest contains many trees. Each tree makes splits, and we average their predictions. A simple baseline always predicts the training average.”

## 3. Read the results (3 minutes)
Say: “We now reveal the hidden outcomes and compare them with the predictions. MAE tells us the average error in percentage points. Dots near the diagonal are closer predictions. These results describe our simulation, not performance on a real plant.”

## 4. Make a new prediction (2 minutes)
Say: “We enter 70% ethanol, 65 degrees, 50 minutes, and 20 mL per gram. The computer predicts recovery; it has not performed this experiment. The result is not necessarily the same as the simplified example in our slides.”

## 5. Discuss trade-offs (3 minutes)
Say: “We can compare many candidate conditions. Higher predicted recovery may require more heating effort. Green points are non-dominated trade-offs. Our effort index is invented and is not kWh or a carbon footprint. We choose a recovery requirement and shortlist low-effort candidates for future experiments.”

## Student task (2 minutes)
Try 50% ethanol, 45°C, 30 minutes and 15 mL/g. Then change only time to 50 minutes. Discuss the prediction change. Increase the minimum recovery requirement from 75 to 80. Compare the shortlist.

Closing: “Machine learning helps us choose experiments to investigate. Laboratory confirmation and actual resource measurements are still essential.”
