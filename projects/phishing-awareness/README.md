# Phishing Awareness Training Project

## Overview
This project is a **Phishing Awareness Training Simulator** built with **Flask**.  
It generates simulated phishing emails, provides awareness landing pages, and tracks user interactions (sent, clicked, reported) on an admin dashboard.

The goal of this project is to help raise security awareness and provide hands-on experience with phishing simulation workflows.

---

## Setup

1. **Create a virtual environment and install dependencies**
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   pip install -r requirements.txt
   
2. **Initialize the database**
   python manage.py init-db

3. **Initialize the database**
   Copy .env.example to .env and adjust campaign defaults.

## Running a Campaign
Run the campaign in preview-only mode (emails saved to /outbox folder).
  python manage.py send --csv recipients.csv --template emails/fake_invoice.html --campaign "October Drill"
  
## Simulation Walkthrough
1.  **Open the phishing email (preview mode).**
2.  **Clicking View Invoice -> Phishing Awareness Debrief page.**
3.  **Clicking Report Simulation -> Reported confirmation page**

## Admin Dashboard
The admin dashboard tracks campaign progress in real-time:
Emails **Sent**

Links **Clicked**

Reports **Submitted**

## Reflections
Learned how phishing awareness simulations are structured.

Hands-on experience with Flask, database handling, and email templates.

Reinforced ethical use: this is for **training and awareness only**, never malicious purposes.
