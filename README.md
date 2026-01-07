# NavonInstFreq

## Analysis pipeline 
Code: Step2_Inst_Freq_Navon.m

### Notes:
I used the FOOOF algorith om the average of this ROI to estimate peak alpha frequency:</br>
roi = {'FC1', 'FC2', 'FC3', 'FC4','FC5', 'FC6', 'C1', 'C2', 'C3', 'C4', 'C5', 'C6', 'Cz', 'CP1', 'CP2', 'CP3', 'CP4', 'CP5', 'CP6', 'CPz', 'P1', 'P2', 'P3', 'P4', 'P5', 'P6', 'P7', 'P8', 'P9', 'P10', 'Pz', 'PO3', 'PO4', 'PO7', 'PO8', 'POz', 'O1', 'O2', 'Oz', 'Iz'};</br>

This gave me a good peak for all participants except 46(35), 40(31),39(30),31(22), 30(21), 29(20), 28(19), 26(17), 23(14), 19(10), 18(9), 14(5), 11(2). I manually adjusted these to 10, so that the GED will enhance any frequencies between 7 and 13 (peak+/-3).

**GED: Why broadband R is better (for your question)**
With R = broadband covariance:
GED asks: “Which spatial pattern has unusually high variance in S relative to overall activity?”
This minimizes frequency locking to the S-band edges.
Small S-band mis-centering (6–12 vs 7–13) rarely changes the selected component.
If the component peak shifts, it’s usually because a different generator was selected, not because the frequency was nudged.
This is exactly what you want when you’re worried about biasing alpha frequency.
