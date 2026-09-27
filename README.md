# stock-market-manipulation
A system to detect irregular market fluctuations.

Every day, retail investors in small-cap US stocks trade under an informational disadvantage that 
the market is supposed to prevent. Pump-and-dump schemes, spoofing, and wash trading quietly 
distort prices in the Russell 2000 - the index of roughly 2,000 small-cap stocks where regulatory 
coverage is thinnest - and by the time a regulator is alerted, the damage to retail capital is already 
done. This project builds and delivers a surveillance system that flips that timeline: flagging high
risk trading activity while it is still forming, not after the crash. 
The surveillance system fuses two complementary signals into a single 0–100 composite risk 
score. The primary signal is an Isolation Forest anomaly detector trained on 467,799 real 2024 
Russell 2000 trading records, validated with F1 = 0.7579, Precision = 0.75, Recall = 0.77 and 
Accuracy = 0.99. The secondary signal, added on the industry mentor's guidance, is a FinBERT 
financial-news sentiment engine that detects manipulation attempts surfacing in company 
narratives before they appear in the price. Every flagged record is accompanied by a plain
language explanation - SHAP feature attribution for compliance analysts, LIME for traders - so 
that every alert can be justified, defended and escalated without ambiguity.
