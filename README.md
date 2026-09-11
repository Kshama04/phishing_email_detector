# phishing_email_detector
A machine learning classifier that detects phishing emails from raw text, built to explore how NLP techniques can support cybersecurity threat detection.

Problem: Phishing remains one of the most common attack vectors for data breaches and credential theft. Automated text-based detection can act as a first line of defense alongside traditional email security tools.

Approach:

Dataset: ~82,000 labeled emails (phishing/legitimate) combining multiple public sources
Preprocessing: lowercasing, URL removal, punctuation stripping
Feature extraction: TF-IDF (top 5,000 terms)
Model: Logistic Regression

Results: 98.1% accuracy, 0.98 precision/recall on both classes. Confusion matrix shows balanced error rates (165 false positives, 145 false negatives out of 16,498 test emails).

Key findings: Top phishing indicators included urgency and financial-bait terms (click, account, bank, investment, remove) and spam-typical products (viagra, replica, watches) — consistent with known social engineering patterns. Legitimate email signals were more domain-specific to the corporate/tech dataset sources.

Limitations: Some legitimate-class signals reflect dataset composition (e.g. company-specific terms) rather than universal "legitimate email" traits — a production system would need broader, more diverse legitimate email sources.

