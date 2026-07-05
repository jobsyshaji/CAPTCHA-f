# CAPTCHA-f
### Security Assessment of CAPTCHA Systems Against Automated Bot Attacks

> A security evaluation project that evaluates the robustness of text-based CAPTCHA systems against automated OCR-based bot attacks by measuring recognition accuracy, solve time, and attack success rate.

---

## Overview

CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart) is one of the most widely used mechanisms for protecting web applications from automated abuse. However, advances in Optical Character Recognition (OCR) and automation frameworks have significantly improved the ability of bots to bypass traditional text-based CAPTCHAs.

**CAPTCHA-f** is an experimental security assessment project developed to analyze the effectiveness of text-based CAPTCHA systems against automated bot attacks. The project simulates real-world attacks using OCR and browser automation to determine how resistant CAPTCHA implementations are to machine-based solving.

The primary objective is to identify vulnerabilities in CAPTCHA design and provide recommendations for improving their resistance against automated attacks.

---

# Objectives

- Evaluate the effectiveness of text-based CAPTCHAs.
- Simulate automated bot attacks using OCR.
- Measure CAPTCHA solving accuracy.
- Analyze character recognition performance.
- Calculate attack success rate.
- Measure average CAPTCHA solving time.
- Identify weaknesses in CAPTCHA generation.
- Recommend improvements for stronger CAPTCHA security.

---

# Features

- Automated CAPTCHA testing
- OCR-based CAPTCHA solving
- Browser automation
- CAPTCHA image preprocessing
- Accuracy measurement
- Performance evaluation
- Result logging
- Security analysis
- Experimental benchmarking

---

# Technology Stack

| Category | Technologies |
|-----------|--------------|
| Language | Python |
| Web Framework | Flask |
| Browser Automation | Selenium |
| OCR Engine | Tesseract OCR |
| Image Processing | Pillow (PIL) |
| Data Analysis | CSV, Python |
| Browser | Google Chrome |
| Driver | ChromeDriver |

---

# System Architecture


             User Request
                  │
                  ▼
          CAPTCHA Generation
                  │
                  ▼
         CAPTCHA Display Page
                  │
                  ▼
       Selenium Automation Bot
                  │
                  ▼
      Capture CAPTCHA Image
                  │
                  ▼
        Image Preprocessing
                  │
                  ▼
          Tesseract OCR
                  │
                  ▼
     Predicted CAPTCHA Text
                  │
                  ▼
      CAPTCHA Verification
                  │
        ┌─────────┴─────────┐
        ▼                   ▼
    Success             Failure
        │                   │
        └─────────┬─────────┘
                  ▼
         Store Experimental Results


---

# Project Workflow

1. Generate random CAPTCHA images.
2. Display CAPTCHA through a Flask web application.
3. Launch automated browser using Selenium.
4. Capture CAPTCHA image.
5. Perform preprocessing on the image.
6. Pass processed image to Tesseract OCR.
7. Extract predicted text.
8. Submit OCR result automatically.
9. Record whether CAPTCHA was solved successfully.
10. Store metrics for analysis.

---

# Experimental Methodology

The assessment follows the following stages:

### Phase 1 — CAPTCHA Generation

Random text-based CAPTCHAs are generated with:

- Random characters
- Different fonts
- Distorted backgrounds
- Noise
- Rotation
- Character spacing variations

---

### Phase 2 — Automated Attack

The CAPTCHA page is accessed using Selenium.

The automation script:

- Opens browser
- Navigates to CAPTCHA page
- Captures CAPTCHA image
- Saves image locally

---

### Phase 3 — Image Preprocessing

Before OCR, images are enhanced using:

- Grayscale conversion
- Noise reduction
- Thresholding
- Contrast enhancement
- Image resizing

These preprocessing steps improve OCR recognition.

---

### Phase 4 — OCR Recognition

Tesseract OCR predicts the CAPTCHA text.

The extracted text is compared with the original CAPTCHA.

---

### Phase 5 — Security Analysis

Collected data is analyzed to determine:

- OCR accuracy
- Success rate
- Solve time
- Character accuracy

---

# Evaluation Metrics

## 1. CAPTCHA Success Rate

Percentage of CAPTCHAs successfully solved.

Formula

```
Success Rate = Successful Solves / Total Attempts × 100
```

---

## 2. Character-Level Accuracy

Measures correctly predicted characters.

```
Accuracy = Correct Characters / Total Characters × 100
```

---

## 3. Average Solve Time

Average time required by the automated attack.

```
Average Time = Total Solve Time / Number of Attempts
```

---

---


# Security Findings

The experimental evaluation revealed several observations:

- Simple text CAPTCHAs are highly vulnerable to OCR attacks.
- Low-noise CAPTCHAs significantly increase bot success rates.
- Standard OCR performs well against predictable fonts.
- Character spacing greatly affects OCR accuracy.
- Background complexity reduces automated recognition.
- Heavy distortion increases CAPTCHA resilience.
- Rotation and overlapping characters decrease OCR performance.

---

# Security Recommendations

To improve CAPTCHA security:

- Introduce stronger character distortion.
- Increase background complexity.
- Add randomized noise.
- Use dynamic fonts.
- Employ variable character spacing.
- Rotate characters independently.
- Implement behavioral analysis.
- Use adaptive CAPTCHA difficulty.
- Integrate invisible CAPTCHA mechanisms.
- Adopt modern challenge-response systems such as reCAPTCHA or hCaptcha where appropriate.

---

# Limitations

- Evaluation focused on OCR-based attacks.
- Deep learning CAPTCHA solvers were not included.
- Audio CAPTCHA was not evaluated.
- Mobile CAPTCHA systems were outside the scope.
- Behavioral CAPTCHA mechanisms were not tested.

---

# Future Improvements

- CNN-based CAPTCHA solver
- Deep Learning OCR
- YOLO-based CAPTCHA segmentation
- Adversarial CAPTCHA generation
- GAN-generated CAPTCHA datasets
- hCaptcha evaluation
- Google reCAPTCHA comparison
- Machine Learning attack detection
- Real-time analytics dashboard

---

# Project Structure


CAPTCHA-f/
│
├── README.md
├── app.py
├── captcha_generator.py
├── bot_attack.py
├── preprocess.py
├── ocr_solver.py
├── requirements.txt
├── results.csv
├── images/
├── screenshots/
├── docs/
└── LICENSE
```

---




---

# Disclaimer

This project was developed solely for academic research and educational purposes. The techniques demonstrated are intended to evaluate CAPTCHA security and improve defensive mechanisms. They should only be used in authorized environments and must not be applied to bypass security protections on systems without explicit permission.

---

