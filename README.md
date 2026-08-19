# TrackLace - Wearable Necklace Tracking System

## Features
- Live GPS tracking (Hardware GPS + Phone GPS fallback)
- Fall detection alerts via SIM800L (SMS & Call)
- Firebase Realtime Database for data storage
- Web dashboard with map and 10-event history

## How it works
1. ESP32 detects a fall and writes `FALL_DETECTED` to Firebase.
2. This website listens for that alert.
3. The website automatically grabs the **phone's GPS** (as a fast fallback).
4. The location is sent back to Firebase.
5. ESP32 reads the command and sends an SMS/Call via SIM800L.
