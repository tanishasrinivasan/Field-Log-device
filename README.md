# FieldLog

FieldLog is a wearable field-reporting device designed for industrial technicians who need to document repair and maintenance work during long shifts.

## Why I Built It

The idea came from a customer discovery call with SubseaFPS, an offshore engineering company.
One of the main pain points I heard was reporting. Technicians can work 12-hour shifts and still need to complete mandatory daily reports afterward. Office staff then collect notes and photos, format the report, review it, and send it to the client before the next morning.
The main insight was that a lot of information is being reconstructed after the work is already finished.
FieldLog is designed to capture that information while the work is happening.

## How It Works

1. The technician approaches a piece of equipment.
2. They tap FieldLog to an NFC tag assigned to that equipment.
3. They press the large record button.
4. They leave a short voice note describing the issue, repair, or work completed.
5. The note is timestamped and associated with that specific asset.
6. Important issues can be flagged using the secondary button.
7. At the end of the shift, the collected logs can be organized into a chronological daily report.

## Current MVP

This MVP focuses on the physical interaction and enclosure design.
The device includes:
- Large glove-friendly record button
- Flag/issue button
- Status display
- Microphone opening
- NFC scanning area
- Belt/vest clip
- USB-C charging port

## Intended Hardware
- ESP32
- NFC module
- MEMS microphone
- LiPo battery
- Push buttons
- Status display/LED
