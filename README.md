# SafeSurf: Phishing Detection and Privacy Protection

## Overview

**SafeSurf** is a browser extension designed to provide **real-time phishing detection and privacy protection**. By leveraging **Large Language Models (LLMs)** like BERT alongside traditional URL blacklisting methods, SafeSurf ensures enhanced security for users browsing the web. The tool detects phishing threats with **97% accuracy**, minimizes false positives, and offers privacy features like **Do Not Track, third-party cookie blocking, and location/camera access control**.

## Features

- **Phishing Detection:** Uses a **hybrid approach** combining URL blacklisting and content-based phishing detection using a fine-tuned **BERT model**.
- **Privacy Protection:** Includes a **privacy toggle** for managing Do Not Track, third-party cookies, location, camera, and microphone access.
- **Real-time Threat Detection:** Queries **Google Safe Browsing, PhishTank, and OpenPhish** databases to check URLs.
- **Machine Learning-Based Content Analysis:** Analyzes webpage text for phishing attempts, going beyond keyword-based methods.
- **Low Latency & Cost-Effective:** Optimized for speed and affordability compared to models like GPT-4.

## System Architecture

SafeSurf is composed of three primary modules:

1. **Phishing Detection Module:**
   - **URL Checking:** Compares URLs against known phishing databases.
   - **Content Analysis Using BERT:** Analyzes webpage text for phishing patterns.

2. **Privacy Management Module:**
   - Allows users to toggle various privacy settings like **third-party cookie blocking, location access, and camera/microphone permissions**.

3. **Proxy Server:**
   - Handles external API requests securely to enhance speed and privacy.

## Dataset and Preprocessing

SafeSurf's phishing detection model was trained on a dataset consisting of **80,000 labeled websites**, including **50,000 legitimate sites** and **30,000 phishing sites** sourced from:

- **Google Search** (for legitimate sites)
- **PhishTank, OpenPhish, PhishRepo** (for phishing sites)

The text is extracted, tokenized using BERT’s tokenizer, and processed to improve detection accuracy.

## Evaluation & Performance

- **97% Accuracy** in phishing detection.
- **High Precision & Recall**, minimizing both false positives and false negatives.
- **Cost-Effective**: Costs **~0.014 cents per request**, compared to **$0.09 per request** for similar GPT-4-based solutions.

### Comparison with Existing Models

| Model           | Accuracy | Latency | Cost per Request |
|---------------|----------|---------|-----------------|
| SafeSurf      | 97%      | Fast    | ~$0.00014      |
| GPT-4 (ChatSpamDetector) | 99.7%   | 12.53s  | $0.09          |
| GPT-3.5       | 96.92%   | 2.5s    | $0.004         |
| Gemini Pro    | 98.06%   | -       | -              |
| Llama2        | 79.05%   | -       | -              |

## User Testing & Feedback

- **100% of users found the extension useful for detecting phishing sites**.
- **93.3% of users** appreciated **automatic updates** from trusted phishing databases.
- Suggested improvements include **ad blocker integration** and **UI customization**.




