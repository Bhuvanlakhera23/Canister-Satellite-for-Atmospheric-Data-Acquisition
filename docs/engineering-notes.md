# Engineering notes

## Design evolution

The 2022–23 preliminary and critical design reviews describe a Teensy-based
payload and a ground-station design that later considered a Vega/ARIES board.
The 2024 report describes a different implementation using two Arduino Nano
controllers linked through I²C. The main page follows that later description.
A single final bill of materials or firmware revision connecting every photograph
to those changes is unavailable, so the diagrams summarize the documented roles.

The records differ in their voltage-monitor and inertial-sensor selections, mass
budgets, enclosure dimensions and antenna specifications. They should be read as
successive design documents, rather than combined into one exact specification.
The SGP40 is listed for a VOC channel; the report's humidity plot has no clearly
identified humidity-sensor model, so humidity is omitted from the component table.

## Data handling and software

The report describes a sensor/telemetry controller, a separate reaction-wheel
controller, radio communication and onboard SD storage. Telemetry fields include
identity, time, packet count, environment, power, GNSS, inertial data and mission
state. The earlier reviews specify a nominal 1 Hz telemetry design and include
command and pressure-input test modes. A design cadence is not a measured rate
for the later hardware.

The mission sequence is boot → idle → launched → descending → parachute deployed
→ landed. The design reviews describe EEPROM logging of state for reset recovery.
The available files contain diagrams, short code illustrations and screenshots,
not a complete firmware tree or a reproducible ground-station build.

## What each figure records

| Public derivative | Original team-report location | Interpretation |
|---|---|---|
| Assembled prototype | PDF p62, Fig30 | Physical enclosure, electronics and mechanism assembly |
| Temperature examples | PDF p60, Fig25 | Separate acquisition/averaging windows, with the original labels retained |
| Radio-test capture | PDF p59, Fig23 | XCTU screenshot; device-address fields cropped out, graph and adverse packet counters retained |
| Ground-station prototype | PDF p62, Fig29 | Interface example; sample values and `nan` fields remain visible |
| Drop-test photographs | PDF p61, Fig28 | Two parachute prototypes with dummy payloads; existing panel layout retained |
| Architecture and data-flow diagrams | Report pp46–49 and 54–55 | New functional summaries, not circuit-board layouts |

The radio image shows 100 sent, 32 received and 68 lost. The displayed 32.00% agrees
with 32/100. There is no timestamped distance record for this capture. It cannot
support a 1 km range claim, a repeatable packet-loss curve or a link-reliability
estimate.

The temperature plots use different horizontal windows and vertical scales. Their
appearance cannot quantify a filter's noise reduction or accuracy. The pressure
illustration elsewhere in the report also contains ambiguous unit labeling; no
numerical sensor-accuracy claim is drawn from it.

## Budgets, estimates and missing raw records

The three-cell series battery configuration is documented, but the power tables
are design calculations using component assumptions. The stated mission duration
is not a measured battery-discharge result. Likewise, the mass figures vary
between design budgets and the later report; this page makes no measured final-mass
claim.

The report discusses drop heights and descent rates without accompanying raw
altitude/time logs. The photographs support the existence of prototype drop work,
not an independently calculated descent-rate distribution. No new flight, radio,
calibration or hardware test was performed to prepare this documentation.
