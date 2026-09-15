# 📡 ELECTROMAGNETIC AUDIO TRANSDUCTION
### Passive RF Rectification, “Rusty Bolt” Audio, and Uniden BC355N Field Operations

[![Status](https://img.shields.io/badge/status-active--field--research-blue)]()
[![Hardware](https://img.shields.io/badge/hardware-Uniden%20BC355N-orange)]()
[![Coverage](https://img.shields.io/badge/coverage-25--956%20MHz-green)]()
[![Region](https://img.shields.io/badge/region-Illinois%20%2F%20FCC%20Chicago-lightgrey)]()
[![License](https://img.shields.io/badge/license-MIT-black)]()

> [!NOTE]
> - **ICC 3086-2026**
> - **FCC #9091647**
> [!WARNING]
> - **This research and report is done by a real person hearing this for real. Hearing a whole conversation next to a HVAC unit with no one there makes you feel crazy until you take a read — everything in the repo below is actually real, researched, documented and needs reported because people have been illegally breaking the law for the longest time. Email is down in the repo below — contact me and I'll give you the source and who they are.**

> **Repository concept:** `DuckyOnQuack-999/ELECTROMAGNETIC-AUDIO-TRANSDUCTION`
> **Purpose:** Document the theory, field logs, scanner procedures, evidence capture, and regulatory reporting path for a reported case of an unmodified AC motor/HVAC chassis producing intelligible audio via passive RF rectification.

---

> [!WARNING]
> **Safety, Legal, and Scope Notice**
> - Do not open, modify, or touch energized AC equipment. Use a licensed electrician for any mains wiring, grounding, or motor work.
> - This repository is for informational, diagnostic, and documentation purposes only. It is not legal, medical, or engineering advice.
> - Many apparent “voices from appliances” are **auditory pareidolia**, local audio leakage, or mechanical noise. This repo provides methods to distinguish real RF demodulation from pareidolia.
> - Frequency numbers in early notes may have been captured during broad scans and are not automatically confirmed sources. Treat all frequencies as **observations until verified**.
> - Do not confront suspected transmitter operators yourself.

---

## 📚 Table of Contents

1. [Executive Summary](#-executive-summary)
2. [Scientific Foundations](#-scientific-foundations)
   - [Electricity Around Us](#1-is-there-electricity-around-us-at-all-times)
   - [Electricity to Transfer Audio](#2-using-electricity-to-transfer-audio)
   - [Wireless Audio Through Air](#3-wireless-audio-through-the-air)
   - [Crosstalk From an AC Motor](#4-crosstalk-from-an-ac-motor)
   - [How an AC Motor Intensifies Audio](#5-how-an-ac-motor-intensifies-audio-over-electricity)
   - [Turning a Motor Into a Speaker](#6-turning-a-motor-into-a-speaker)
   - [Miles Away vs. Right Next to You](#7-unmodified-motor-miles-away-vs-right-next-to-you)
   - [Can Anyone Hear This?](#8-can-a-normal-non-autistic-person-hear-this)
3. [Passive Intermodulation / “Rusty Bolt” Effect](#-passive-intermodulation--rusty-bolt-effect)
4. [Full System Transduction Diaphragm](#-full-system-transduction-diaphragm)
5. [Observation Logs & Telemetry](#-observation-logs--telemetry)
6. [Hardware Manual: Uniden BC355N](#-hardware-manual-uniden-bc355n)
7. [Field Operations Guides](#-field-operations-guides)
8. [Evidence Capture Protocol](#-evidence-capture-protocol)
9. [Regulatory & Law Enforcement Reporting](#-regulatory--law-enforcement-reporting)
10. [Electric Utility Company Contact Directory](#-electric-utility-company-contact-directory)
11. [Physical Mitigation](#-physical-mitigation)
12. [AI Research Prompt](#-ai-research-prompt)
13. [Appendices](#-appendices)
14. [Omissions Audit & Verification](#-omissions-audit--verification)

---

## 🧭 Executive Summary

This repository merges the entire research thread into one field-ready document.

Key conclusions:

- **Electricity is everywhere** — in the atmosphere, inside matter, and inside the human body.
- **Audio can be transferred by electricity** — microphones convert sound to electrical signals; speakers convert them back.
- **Audio can be transferred wirelessly through air** — via radio waves, infrared light, or laser beams.
- **AC motors can cause crosstalk** — through magnetic induction, dirty power, and ground loops.
- **A motor can be turned into a speaker** — by feeding amplified audio into its coils and using its casing as a diaphragm.
- **An unmodified motor miles away cannot transmit audio** — but an unmodified motor **right next to you** may accidentally demodulate strong RF via the “Rusty Bolt” effect, or the sound may be pareidolia.
- **Anyone can experience this** — neurotypical and autistic people alike.
- **The Uniden BC355N** is the field scanner used here. It is DC-powered, covers 25–956 MHz, and has Close Call RF Capture.
- **462.8875 MHz was not the target** — it was a baseline scan capture. The logged target observations are **917.5000 MHz**, **865.5000 MHz**, and **937.0250 MHz**.
- **917.5000 MHz** is in the 902–928 MHz ISM band. It is usually digital data, but analog voice can appear from older cordless phones, baby monitors, wireless mics, or illegally amplified Part 15 gear.
- **865.5000 MHz** is logged as a spectral shift capture. If voices are heard here that sound like harassment or role-play, report immediately to the agencies listed in [Regulatory & Law Enforcement Reporting](#-regulatory--law-enforcement-reporting).
- **937.0250 MHz** is logged as an additional capture. It sits **outside** the standard ISM band and likely belongs to a different service class.
- **Electric utility companies** own and operate the power lines, transformers, meters, and grid infrastructure that can act as **accidental antennas** in passive RF rectification scenarios. They must be contacted first before escalating to the FCC or ICC.
- **Reporting paths:** Electric utility companies (ComEd, Ameren, MidAmerican), ICC, FCC Chicago Field Office, FBI, APCO, and Illinois State Police TSB.
- **Mitigation:** snap-on ferrite chokes, proper grounding, shielded cables, 90° crossing, and power isolation.

---

## 🔬 Scientific Foundations

### 1. Is There Electricity Around Us at All Times?

**Yes.** Weak electric fields, charged ions, static forces, and natural electricity surround us and exist inside us.

#### In the Air and Atmosphere

- Earth has a **global electric circuit**.
- On clear days, air above ground is positively charged; ground is negatively charged.
- Fair-weather electric field near the ground: **about 100 volts per meter**.
- Cosmic rays and solar radiation create **ions** in the air.
- Wikipedia notes: “the atmospheric electric field is negatively directed (meaning toward the ground) in fair weather.”

#### Inside All Matter

- Atoms contain **positively charged protons** and **negatively charged electrons**.
- Opposite charges attract and hold atoms/molecules together.
- Without electrostatic forces, matter could not exist in its normal shape.

#### Inside the Human Body

- Cells use tiny electrical signals.
- Nerves send electrical impulses.
- The heart’s rhythm is controlled by electrical currents.
- SparkFun Learn: electricity is at work “from the lightning in a thunderstorm to the synapses inside our body.”

---

### 2. Using Electricity to Transfer Audio

Yes. Electricity is the primary way we capture, transfer, and play back audio.

#### The 3-Step Process

```mermaid
flowchart LR
    A[Sound Wave] --> B[Microphone / Input]
    B --> C[Electrical Signal / Wire]
    C --> D[Speaker / Output]
    D --> E[Sound Wave]
```

1. **Conversion to Electricity (Input):**
   A microphone diaphragm moves a magnet/coil, creating a fluctuating electrical current matching the sound.

2. **Transmission (Wire):**
   The varying current travels through conductive copper wires. Voltage rises/falls in a pattern mirroring the sound wave.

3. **Conversion Back to Sound (Output):**
   A speaker coil near a magnet moves a cone, vibrating air and recreating sound.

#### Analog vs Digital Audio

| Format | How It Works | Examples |
|---|---|---|
| **Analog Audio** | Voltage continuously fluctuates in direct proportion to the sound wave. | 3.5mm headphone jacks, XLR studio mics, instrument cables |
| **Digital Audio** | Analog wave is sampled millions of times per second and converted to binary 1s/0s. | USB audio, HDMI, coaxial digital cables |

---

### 3. Wireless Audio Through the Air

Electricity cannot travel through air on its own without dangerous high-voltage sparking. Instead, devices use electricity to generate **electromagnetic waves**.

#### Three Main Methods

| Method | How It Works | Examples |
|---|---|---|
| **Radio Frequency (RF)** | Electrical audio signal feeds a transmitter; antenna converts current to radio waves; receiver converts back. | AM/FM, Bluetooth, Wi-Fi |
| **Infrared Light (IR)** | Audio signal drives an IR LED that flickers; photodiode receives and converts back to current. | Wireless headphones, remote audio |
| **Laser / Li-Fi** | Audio voltage modulates laser brightness; solar panel/light sensor converts back to current. | DIY laser audio experiments |

#### Universal 3-Step Formula

```mermaid
flowchart LR
    A[Encode: Electricity to Modulated Pattern] --> B[Transmit: Radio or Light Wave]
    B --> C[Decode: Wave to Electricity to Speaker]
```

---

### 4. Crosstalk From an AC Motor

You hear crosstalk from an AC motor because the motor acts as an **aggressor** and your audio equipment acts as a **victim**.

An AC motor pulls large fluctuating currents. This creates electromagnetic chaos that can enter audio components as hum, buzz, or whine.

#### Three Primary Entry Points

| Entry Point | Mechanism | Result |
|---|---|---|
| **Magnetic / Inductive Coupling** | Motor’s spinning magnetic fields cut across unshielded audio cables. | Induced current treated as audio. |
| **Power-Line Modulation (“Dirty Power”)** | Motor spikes distort the 60 Hz sine wave; harmonics enter power lines. | Noise bypasses power supply into amplification stage. |
| **Shared Ground Loops** | Motor dumps stray current into common ground. | Voltage difference causes loud continuous hum. |

#### Diagnosis and Fixes

- Physically separate audio gear from motor and power lines.
- Cross wires at **90 degrees**, never parallel.
- Use **shielded cables** or balanced XLR.
- Plug audio into an **isolated power conditioner** or different circuit.
- Check ground connections.

---

### 5. How an AC Motor Intensifies Audio Over Electricity

An AC motor does not “amplify” music helpfully. It **modulates**, **distorts**, and **overrides** the audio signal.

| Mechanism | What Happens | What You Hear |
|---|---|---|
| **Amplitude Modulation** | Motor’s magnetic fields fluctuate resistance/inductance in nearby audio components. | Tremolo/fluttering effect. |
| **Microphonic Induction** | Physical vibration shakes audio components, which act like microphones. | Booming feedback/rumble. |
| **Harmonic Distortion / Superposition** | Motor’s 50/60 Hz and harmonics add to audio wave. | Loud buzz/whine drowning out original sound. |

---

### 6. Turning a Motor Into a Speaker

Yes — a motor and a speaker share the same core concept: **coils of wire around magnets**.

| Device | How It Works |
|---|---|
| **Speaker** | Audio current through coil creates shifting magnetic field; moves cone; vibrates air. |
| **Motor** | Current through coil creates shifting magnetic field; pushes rotor in circles. |

#### Basic DIY Motor Speaker

1. **Wiring:** Run audio output into an audio amplifier (e.g., LM386). Connect amplifier output to motor power leads.
2. **Sound Production:** Audio current rapidly shifts direction; motor shaft vibrates instead of spinning fully.
3. **Acoustic Volume:** Hot-glue motor casing to a plastic cup or paper plate to act as a speaker cone.
4. **Examples:** Hoverboards/Segways beep through motors; 3D printers play tunes through stepper motors.

> [!NOTE]
> This only works when the motor is **driven by an audio signal**. An unmodified motor far away cannot transmit audio.

---

### 7. Unmodified Motor Miles Away vs. Right Next to You

| Scenario | Possible? | Explanation |
|---|---|---|
| **Unmodified motor miles away transmits audio** | **No** | No microphone, no data input, heavy inertia, severe distance limitations. |
| **Unmodified motor right next to you plays audio** | **Possible, rare** | Passive Intermodulation / “Rusty Bolt” effect, or auditory pareidolia. |

#### If You Are by the Motor

You may be witnessing:

- **Passive Intermodulation (PIM)** — metal-oxide junction acts as a crude diode.
- **Accidental crystal radio behavior** — wiring acts as antenna; corrosion acts as demodulator; motor plates act as speaker.
- **Auditory pareidolia** — brain finds patterns in motor noise.

---

### 8. Can a Normal, Non-Autistic Person Hear This?

**Yes.** Both phenomena are universal.

- **Physical radio phenomenon:** Real acoustic sound waves; anyone with standard hearing can hear it. A phone recording will capture it.
- **Auditory pareidolia:** A fundamental human brain trait. Anyone can experience it, especially when tired, stressed, or in a quiet room with continuous noise.

> **Test:** Record the motor with your phone. If the audio disappears on the recording and you only hear motor hum, it is likely pareidolia. If the recording captures the voices, it is a physical acoustic event.

---

## 📡 Passive Intermodulation / “Rusty Bolt” Effect

### Abstract

This section documents the hypothesis that an unmodified AC motor/HVAC chassis can accidentally act as an analog radio receiver.

The system mimics:

1. **Antenna**
2. **Demodulator**
3. **Acoustic transducer**

### Three-Stage Demodulation Loop

```mermaid
graph TD
    Transmitter[📡 High-Power External Transmitter]
    AirborneWave(⚡ Airborne Radio Waves)

    subgraph Stage1 [STAGE 1: ACCIDENTAL RESONANT ANTENNA]
        Ductwork[Sheet-Metal Ductwork]
        Pipes[Copper Refrigerant Lines]
        Chassis[Metallic Enclosure Frame]
    end

    subgraph Stage2 [STAGE 2: PASSIVE DIODE RECTIFIER]
        Oxidation[Microscopic Rust / Metal-Oxide]
        Junction[Corroded Mounting Brackets / Threads]
    end

    subgraph Stage3 [STAGE 3: MECHANICAL SPEAKER TRANSDUCTION]
        Coils[Motor Copper Windings]
        Stator[Steel Stator Plates]
    end

    AcousticWaves((🔊 Audible Sound Waves In Room))

    Transmitter -->|Pushes Electromagnetic Field| AirborneWave
    AirborneWave -->|Matches Physical Structure Length| Stage1
    Stage1 ==>|Induces Alternating RF Current| Stage2
    Stage2 ==>|Strips Carrier / Leaves Audio Current| Stage3
    Stage3 -->|Magnetic Fields Force Metal to Flex| AcousticWaves

    classDef federal fill:#8a2be2,stroke:#333,stroke-width:2px,color:#fff;
    classDef physical fill:#1e90ff,stroke:#333,stroke-width:2px,color:#fff;
    classDef internal fill:#2f4f4f,stroke:#333,stroke-width:1px,color:#fff;

    class Transmitter,AirborneWave federal;
    class AcousticWaves physical;
    class Ductwork,Pipes,Chassis,Oxidation,Junction,Coils,Stator internal;
```

### Stage 1: RF Induction — The Accidental Antenna

- HVAC ductwork, copper refrigerant lines, structural framing, and electrical conduits act as an unintentional resonant antenna.
- High-power radio waves strike metal surfaces.
- Electromagnetic fields force free electrons to vibrate.
- This induces a high-frequency alternating current in the appliance frame.

### Stage 2: Passive Rectification — The Accidental Diode

- RF carrier waves oscillate millions of times per second.
- This is too fast to vibrate heavy steel plates audibly.
- Where metal touches imperfectly — rust, loose threads, oxidized brackets — a **metal-oxide junction** forms.
- This junction acts like a crude semiconductor diode.
- It allows current in one direction, stripping the RF carrier and leaving low-frequency audio current.

### Stage 3: Acoustic Transduction — The Accidental Speaker

- Audio current enters the motor’s dense copper stator coils.
- The current creates a shifting magnetic field pulsing at voice frequencies (300–3,000 Hz).
- The motor shaft cannot spin fast enough, so stator plates and casing flex and vibrate.
- The machine casing acts as a speaker cone, pushing audible sound into the room.

### Mermaid Sequence View

```mermaid
sequenceDiagram
    participant TX as External Transmitter
    participant METAL as HVAC Metal / Wiring
    participant DIODE as Rusty / Oxidized Junction
    participant MOTOR as AC Motor Windings
    participant AIR as Room Air

    TX->>METAL: Airborne RF wave
    METAL->>DIODE: Induced high-frequency current
    DIODE->>MOTOR: Rectified audio current
    MOTOR->>AIR: Mechanical vibration / sound
    AIR-->>Listener: Audible voice or audio
```

### Prime External Signal Sources

| Source | Power / Notes | Why It Can Bleed |
|---|---|---|
| **High-Power AM Broadcast Towers** | 10,000–50,000 W | Amplitude modulation; large waves; highly susceptible to passive rectification. |
| **Amateur (Ham) Radio Operators** | Up to 1,500 W | High-wattage transmissions; antenna proximity; structural resonance. |
| **CB Operators with Linear Amplifiers** | Illegal boost from 4 W to hundreds/thousands | Overpowered local signal floods household wiring. |
| **Unlicensed Long-Range Part 15 Gear** | Illegal external amplifiers | Baby monitors, wireless mics, older cordless phones modified for long range. |
| **GMRS / Land Mobile Repeaters** | Up to 50 W | High local RF density; can induce currents in unshielded metal. |
| **Electric Utility Infrastructure** | Smart meters, SCADA, power line arcing | Broadband noise from arcing insulators, loose hardware, failing arresters; digital data bursts from AMI meters. |

### Frequency Band Context

| Frequency | Band / Service | Typical Use | Notes |
|---|---|---|---|
| **462.8875 MHz** | GMRS Channel 20 (Repeater Output) | Two-way voice, up to 50 W | Baseline scan capture only, not the confirmed target. |
| **865.5000 MHz** | Sub-900 MHz land mobile / utility | Voice or data depending on license | Logged as a spectral shift capture; service not fully decoded. If voices sound like harassment or role-play, report to FCC / FBI. |
| **917.5000 MHz** | 902–928 MHz ISM band | Smart meters, LoRaWAN, RFID, older analog cordless phones, baby monitors, wireless mics | Usually digital; voice implies analog consumer gear or illegal amplification. |
| **937.0250 MHz** | **Outside** standard ISM band (928–960 MHz) | Fixed microwave links, land mobile, certain Part 15 devices, utility SCADA | Additional capture; requires modulation/call sign logging to identify service. |
| **530–1700 kHz** | AM Broadcast Band | Commercial AM radio | BC355N does **not** cover this; use a separate portable AM radio. |

### Frequency Notes

- **462.8875 MHz** — GMRS Channel 20 repeater output. In the thread, this was a **baseline scan capture**, not the confirmed target.
- **917.5000 MHz** — 902–928 MHz ISM band. Usually digital data: smart meters, LoRaWAN, RFID, industrial sensors. If voice is heard, possible older analog cordless phone, wireless mic, baby monitor, or illegally amplified Part 15 device.
- **865.5000 MHz** — Logged as a spectral shift capture. Not fully decoded in the thread. Could be image/intermod, land mobile, or other local transmitter. Log and report. If voices sound like harassment or role-play, report to the agencies listed in [Regulatory & Law Enforcement Reporting](#-regulatory--law-enforcement-reporting).
- **937.0250 MHz** — **Outside** the standard 902–928 MHz ISM band. Falls in 928–960 MHz, used for fixed microwave links, land mobile radio, certain Part 15 devices, and utility SCADA. Voice here is more likely a licensed business, land mobile, or public safety transmitter than a smart meter. Log modulation type (AM/FM/NFM), bandwidth, and any call signs or identifiers to identify the service and whether it is operating legally.
- **AM Broadcast Band (530–1700 kHz)** — The BC355N does **not** cover this. Use a standard portable AM radio to check for commercial AM broadcast bleed.

---

## 🧬 Full System Transduction Diaphragm

```text
[ AM / FM / TWO-WAY RF SOURCE ]
              │
              │  (Airborne Radio Waves Wave-Matching to ~25.5" Conduit Structures)
              ▼
 ┌──────────────────────────────────────────────────────────┐
 │ STAGE 1: ACCIDENTAL RESONANT ANTENNA                     │
 │ • Galvanized Sheet Metal Ductwork                        │
 │ • Bare Copper Fluid Refrigerant Lines                    │
 │ • Structural Metallic Equipment Enclosure                │
 └────────────────────────────┬─────────────────────────────┘
                              │
                              │ (Induced High-Frequency Alternating Current)
                              ▼
 ┌──────────────────────────────────────────────────────────┐
 │ STAGE 2: PASSIVE SEMICONDUCTOR RECTIFIER                 │
 │ • Corroded Mounting Screws & Oxidized Brackets           │
 │ • Loose Conduit Coupling Threads                         │
 │ [Metal] ──> [Microscopic Rust / Metal-Oxide] ──> [Metal] │
 └────────────────────────────┬─────────────────────────────┘
                              │
                              │ (RF Carrier Stripped / Low-Frequency Audio Current Left)
                              ▼
 ┌──────────────────────────────────────────────────────────┐
 │ STAGE 3: ACOUSTIC TRANSDUCTION MECHANICAL SPEAKER        │
 │ • Fluctuating Audio Current Enters Dense Motor Windings   │
 │ • Rapidly Shifting Magnetic Field Created in Core         │
 │ • Heavy Steel Stator Plates Physically Flex and Rattle    │
 └────────────────────────────┬─────────────────────────────┘
                              │
                              │ (Mechanical Micro-Vibrations Shaking Casing Housing)
                              ▼
                 [ AUDIBLE SOUND WAVES IN AIR ]
```

### Transduction Definition

In physics and engineering, **transduction** is the conversion of one form of energy into another. A device that does this is a **transducer**.

| Everyday Example | Energy In | Energy Out |
|---|---|---|
| **Microphone** | Acoustic (sound waves) | Electrical (audio current) |
| **Speaker** | Electrical (audio current) | Acoustic (sound waves) |
| **Motor-as-speaker (accidental)** | Electrical/magnetic | Acoustic (sound waves) |

The motor-speaker transduction chain: **audio current → shifting magnetic field → physical flex of stator plates and casing → air pressure waves → audible sound.**

---

## 📊 Observation Logs & Telemetry

### Sound Frequency / Time Observation Log

**Contact registers:** `cl2344@gmail.com`, `joshinhd1@gmail.com`

| # | Date | Time Window | Target Frequency | Detection Type | Active Duration |
|---:|---|---|---|---|---|
| 01 | September 9, 2026 | 12:00 AM – 03:00 AM | 917.5000 MHz | Acoustic Demodulation Event | ~180 min (3.0 h) |
| 02 | September 13, 2026 | 02:35 AM – 03:06 AM | 917.5000 MHz | Acoustic Demodulation Event | ~31 min |
| 03 | September 14, 2026 | 01:25 PM – 01:35 PM | 917.5000 MHz | Acoustic Demodulation Event | ~10 min |
| 04 | September 14, 2026 | 02:15 PM – 02:25 PM | 865.5000 MHz | Spectral Shift Capture | ~10 min |
| 05 | September 15, 2026 | (time not logged) | 937.0250 MHz | Additional Capture | Not logged |

### 📡 Frequency Master Log (Editable Master)

|  # | Date           | Start Time | End Time | Frequency        | Occurrences | Signal / Strength | Notes |
| -: | -------------- | ---------- | -------- | ---------------- | ----------: | ----------------- | ----- |
|  1 | Sept. 9, 2026  | 12:03 AM   | —        | **917.5000 MHz** |           1 | —                 |       |
|  2 | Sept. 13, 2026 | 2:35 AM    | 3:06 AM  | **917.5000 MHz** |           1 | —                 |       |
|  3 | Sept. 14, 2026 | —          | —        | **917.5000 MHz** |           1 | —                 |       |
|  4 | Sept. 14, 2026 | —          | —        | **865.5000 MHz** |           1 | —                 |       |
|  5 | Sept. 15, 2026 | —          | —        | **937.0250 MHz** |           1 | —                 |       |

### 📊 Frequency × Date Matrix

| Frequency        | Sept. 9 | Sept. 13 | Sept. 14 | Sept. 15 | **Total Recorded** |
| ---------------- | ------: | -------: | -------: | -------: | -----------------: |
| **917.5000 MHz** |       1 |        1 |        1 |        0 |              **3** |
| **865.5000 MHz** |       0 |        0 |        1 |        0 |              **1** |
| **937.0250 MHz** |       0 |        0 |        0 |        1 |              **1** |
| **Daily Total**  |   **1** |    **1** |    **2** |    **1** |              **5** |

### Frequency Summary

| Frequency | Sept. 9 | Sept. 13 | Sept. 14 | Sept. 15 | Total Recorded Occurrences |
|---|---:|---:|---:|---:|---:|
| **917.5000 MHz** | ✓ | ✓ | ✓ |  | 3 |
| **865.5000 MHz** |  |  | ✓ |  | 1 |
| **937.0250 MHz** |  |  |  | ✓ | 1 |

### 📈 Frequency Occurrence Chart

```mermaid
xychart-beta
    title "Recorded Frequency Occurrences"
    x-axis ["917.5000 MHz", "865.5000 MHz", "937.0250 MHz"]
    y-axis "Occurrences" 0 --> 3
    bar [3, 1, 1]
```

### Frequency Occurrence Totals (Simple Table)

Total recorded occurrences for each monitored frequency through September 15, 2026.

| Frequency | Occurrences |
|---|---:|
| 917.5000 MHz | 3 |
| 865.5000 MHz | 1 |
| 937.0250 MHz | 1 |

### 📅 Daily Activity

| Date               | Frequencies Recorded                     | Total Occurrences |
| ------------------ | ---------------------------------------- | ----------------: |
| **Sept. 9, 2026**  | 917.5000 MHz                             |             **1** |
| **Sept. 13, 2026** | 917.5000 MHz                             |             **1** |
| **Sept. 14, 2026** | 917.5000 MHz, 865.5000 MHz               |             **2** |
| **Sept. 15, 2026** | 937.0250 MHz                             |             **1** |
| **Grand Total**    | **3 unique frequencies**                 |             **5** |

### 📅 Chronological Timeline

```mermaid
timeline
    title Recorded Sound Events
    September 9, 2026 : 12:00 AM–3:00 AM : 917.5000 MHz
    September 13, 2026 : 2:35 AM–3:06 AM : 917.5000 MHz
    September 14, 2026 : 1:25 PM–1:35 PM : 917.5000 MHz
    September 14, 2026 : 2:15 PM–2:25 PM : 865.5000 MHz
    September 15, 2026 : (time not logged) : 937.0250 MHz
```

> [!NOTE]
> These frequencies are **reported measurements/observations**. No source or cause is inferred solely from these numbers. Additional observations can be appended chronologically without altering historical entries.

### 🔧 Master Editable Fields

For future entries, the most useful columns are:

**Date → Start → End → Frequency → Occurrences → Signal strength → Modulation → Bandwidth → Location/Direction → What was heard → Notes**

That way, a frequency can occur **multiple times on the same day** without losing information, while the summary table can still show one clean row per frequency.

---

## 🎛️ Hardware Manual: Uniden BC355N

The Uniden BC355N is a compact, multi-band **analog** mobile/base radio scanner.

### Key Specifications

| Feature | Detail |
|---|---|
| **Frequency Coverage** | 25 MHz – 956 MHz |
| **Channels** | 300 programmable |
| **Modes** | AM, FM, analog only |
| **Close Call** | Yes — RF Capture Technology |
| **Power** | 13.8 V DC |
| **Home Power** | AC-to-DC wall adapter |
| **Vehicle Power** | DC cigarette lighter cord |
| **Bands** | CB, Ham, Aircraft, Marine, Police/Fire/Emergency, Weather, 800 MHz |
| **Limitation** | Does not receive standard AM broadcast band 530–1700 kHz |

### Control Layout

```text
+-------------------------------------------------------------+
|                                                             |
|  [ SQUELCH (SQ) ]                              [ DISPLAY ]  |
|  [ VOLUME (VOL) ]                             (Orange Back) |
|                                                             |
|  [HOLD]       [UP (▲)]      [DOWN (▼)]      [ 800 MHz ]     |
|  [PRIVATE]    [PD/FD/EMG]   [AIR/MRN]                       |
|  [🎯 CC]      [WX]          [CB]                            |
|                                                             |
|         [SEARCH]      [L/O]         [BAND]        [PROG]    |
+-------------------------------------------------------------+
```

### Full Button & Control Run-Down

| Control | Location | Function |
|---|---|---|
| **VOLUME / POWER** | Bottom-left knob | Turns unit on/off; adjusts audio output. |
| **SQUELCH (SQ)** | Top-left knob | Mutes background static. Turn CCW until hiss, then CW until static snaps shut. |
| **HOLD** | Top-left keypad, red dot | Freezes scanner on current frequency. Press again to release. |
| **UP (▲) / DOWN (▼)** | Top row | Manually step frequencies or change scan direction. |
| **800 MHz** | Top-right | Jumps to preprogrammed 800 MHz bank. |
| **PRIVATE** | Left, second row | Accesses user-programmed memory slots. |
| **PD/FD/EMG** | Middle row | Scans preprogrammed police/fire/emergency analog frequencies. |
| **AIR/MRN** | Middle row | Toggles civil aviation AM and VHF marine bands. |
| **🎯 CLOSE CALL (CC)** | Bottom-left | Activates Close Call RF Capture. |
| **WX** | Bottom row | Scans 7 NOAA weather channels. |
| **CB** | Bottom row | Scans 40 standard CB channels (26.965–27.405 MHz). |
| **SEARCH** | Bottom row | Starts manual frequency search between band limits. |
| **L/O** | Bottom row | Lockout — skips current frequency in future scans. |
| **BAND** | Bottom row | Cycles through factory frequency blocks. |
| **PROG** | Bottom-right | Enters program mode to store active frequency. |

### Close Call Modes

```mermaid
stateDiagram-v2
    [*] --> Normal
    Normal --> BackgroundCC: Tap 🎯 once
    BackgroundCC --> CCOOnly: Hold 🎯 2 sec
    CCOOnly --> Off: Tap 🎯 again
    Off --> Normal: Tap 🎯 again
    BackgroundCC: Target icon steady
    CCOOnly: Screen flashes "CC Only"
    Off: Target icon disappears
```

| Mode | How to Enter | Behavior |
|---|---|---|
| **Background CC Priority** | Tap 🎯 once | Scans normal channels but checks for local RF every 2 seconds. |
| **Dedicated CC Only** | Hold 🎯 2 seconds | 100% processing power on local RF capture. Best next to motor. |
| **Close Call Off** | Tap 🎯 again | Deactivates local RF capture. |

### Lockout (L/O)

- When scanner stops on unwanted frequency, tap **L/O** once.
- Scanner skips it permanently.
- To clear a lockout, hold **L/O** for 2 seconds while on that band.

### Display Codes

| Code | Meaning |
|---|---|
| **CAn 5** | A channel or search block has been canceled/cleared. |
| **CLEAr** | Master reset confirmed; memory registers wiped. |
| **CC Only** | Dedicated Close Call mode active. |

### Power: DC Powered

- The BC355N is powered by **13.8 V DC**.
- Home: AC-to-DC wall adapter.
- Vehicle: DC cigarette lighter cord.
- Back panel: standard black DC barrel plug.

---

## 🕹️ Field Operations Guides

### GUIDE 1: Complete Hardware Master Reset

Use this to clear old lockouts, saved channels, and registers.

```bash
# 1. Turn VOLUME knob fully counterclockwise to OFF
# 2. Press and hold: [HOLD] + [L/O] + [PROG]
# 3. While holding, turn VOLUME knob clockwise to ON
# 4. Hold 3 seconds until screen flashes:
CLEAr
# 5. Release keys
```

### GUIDE 2: Clean Close Call Only Scan

```bash
# 1. Master reset first if memory is cluttered
# 2. Turn SQUELCH (SQ) clockwise until background static snaps shut
# 3. Press and hold 🎯 CLOSE CALL for 2 seconds
# 4. Verify screen shows:
CC Only
# 5. Place antenna against HVAC/motor housing
# 6. When signal hits, press HOLD to freeze frequency
```

### GUIDE 3: Save Discovered Frequency to Private Bank

Because the BC355N has no numeric keypad:

```bash
# 1. Ensure target frequency is frozen on screen with HOLD
# 2. Press PROG once
# 3. An empty channel slot blinks (e.g., Ch 01)
# 4. Press and hold PRIVATE for 2 seconds
# 5. Listen for BEEP
# 6. Tap PRIVATE to monitor saved channel
```

### GUIDE 4: Lock Out Unwanted Frequencies

```bash
# When scanner stops on unwanted signal:
Press L/O once
# Scanner resumes; frequency is skipped in future scans
```

### GUIDE 5: Scanning CB, Ham, and AM Broadcast

| Target | Scanner Action | Notes |
|---|---|---|
| **CB** | Press CB | 40 channels; 26.965–27.405 MHz. |
| **Ham** | Press SEARCH then BAND | Check 28.000–29.700 MHz, 50–54 MHz. |
| **AM Broadcast** | Use separate portable AM radio | BC355N does not cover 530–1700 kHz. |

### GUIDE 6: Using a Radio Receiver to Pick Up the Signal

1. Use a portable shortwave/AM receiver or SDR.
2. Scan standard AM broadcast band.
3. Scan CB band.
4. Scan Ham bands.
5. When audio matches motor audio at same split-second, log frequency and signal strength.
6. Use **Tecsun PL-330/PL-880** or **RTL-SDR Blog V4** for advanced tracking.

### GUIDE 7: Best Equipment to Capture Evidence

| Purpose | Recommended Gear | Why |
|---|---|---|
| **Acoustic capture** | Zoom F-Series, Tascam recorder | Shielded, balanced XLR inputs. |
| **Directional mic** | Sennheiser MKH-416, E-Image PM-510 | Isolates motor sound from room. |
| **RF measurement** | GQ EMF-390, LATNEX HF-B3G | Measures RF spikes; data logging. |
| **Scanner** | Uniden BC355N | Close Call, analog voice, 25–956 MHz. |
| **Phone** | Any modern smartphone | Video + audio dual-source proof. |

### GUIDE 8: Handling 917.5000 MHz

- BC355N **can** pick up 917.5000 MHz (coverage 806–956 MHz).
- Usually digital data: smart meters, LoRaWAN, RFID.
- If you hear talking:
  - Older 900 MHz cordless phone.
  - 900 MHz wireless microphone.
  - Analog baby monitor.
  - Illegally amplified Part 15 device.
- If unwanted, press **L/O** to skip.
- If heard any voices especially on **865.5000 MHz** that sounds like harassment or role-play, report to the following:
  - [Regulatory & Law Enforcement Reporting](#-regulatory--law-enforcement-reporting).

### GUIDE 9: Handling 937.0250 MHz

- 937.0250 MHz is **outside** the 902–928 MHz ISM band.
- It falls in the 928–960 MHz range, which in the US includes fixed microwave links, land mobile radio, utility SCADA, and certain Part 15 devices.
- Voice on this frequency is more likely a licensed transmitter than a smart meter.
- Log: modulation type (AM/FM/NFM), bandwidth, call signs, identifiers, time patterns.
- If it causes harmful interference, include it in FCC and FBI reports with the exact frequency.

### GUIDE 10: Contacting Your Electric Utility

If you suspect power-line hardware, smart meters, or utility-owned equipment is contributing to the interference:

1. **Find your utility** on your electric bill or via the ICC utility lookup.
2. **Call the utility’s customer service** and ask for a **“power quality”** or **“RF interference”** investigation.
3. **Provide:** account number, service address, pole number (if known), and a chronological log of interference events.
4. **Reference IEEE 1897-2024** — the standard for locating power-line gap interference sources.
5. **If unresolved:** File an informal complaint with the ICC at 1-800-524-0795.
6. **If still unresolved:** File a formal ICC complaint and escalate to the FCC.

---

## 📋 Evidence Capture Protocol

### Dual-Source Acoustic Verification Test

```mermaid
flowchart TD
    A[Place scanner next to motor] --> B[Lock scanner on target frequency]
    B --> C[Start smartphone video]
    C --> D[Record wide shot: motor + scanner]
    D --> E[Move mic close to motor casing]
    E --> F[Capture scanner audio + motor audio at same split-second]
    F --> G[While recording, unplug motor safely]
    G --> H{Motor audio stops?}
    H -->|Yes, scanner continues| I[Definitive proof of passive rectification]
    H -->|No, both stop| J[Re-evaluate source / pareidolia]
```

### Logging Template

```markdown
| # | Date | Time Window | Frequency | What Was Heard | Duration | Notes |
|---:|---|---|---|---|---|---|
| 1 | YYYY-MM-DD | HH:MM–HH:MM | XXX.XXXX MHz | Voice/music/tone | XX min | Weather, motor speed, etc. |
```

### FCC Complaint Template

```text
TECHNICAL ASSISTANCE REQUEST: PASSIVE INTERMODULATION / UNAUTHORIZED TRANSMISSION
Target Frequency: [Insert confirmed scanner frequency]
Reporting Region: Illinois / FCC Chicago Field Office Jurisdiction
Affected Hardware: Unmodified Residential HVAC System / AC Induction Motor
Diagnostic Tool: Uniden BC355N Analog Base/Mobile Receiver

Description:
A high-power external radio frequency transmission is actively causing heavy electromagnetic interference within my residence. The stray RF field is inducing an alternating current across unshielded structural metal and copper plumbing lines associated with my household HVAC system. Due to an accidental metal-oxide junction (diode effect) within the appliance chassis, this signal is being passively rectified, forcing raw audio-frequency current into the stator windings of an unmodified AC motor. The physical casing of the motor is subsequently transducing this current into audible acoustic waves.

Using a dedicated analog receiver positioned directly at the motor chassis, the invading signal has been isolated and logged. The signal density is sufficient to mechanically drive heavy motor plates, indicating the likely presence of an overpowered, poorly filtered, or unauthorized high-gain local transmitter operating in immediate geographic proximity to this residence. Chronological time logs and synchronized dual-source audio recordings demonstrating passive rectification are prepared for analysis by FCC field enforcement agents.
```

### FBI Tip Template

```text
SUBJECT: REPORT OF UNAUTHORIZED LONG-RANGE TRANSMISSIONS / INTERCEPTED VOICE COMMUNICATIONS

LOCATION OF OBSERVATION: [City, State, neighborhood]
FREQUENCY DETECTED: [Frequency] MHz (Analog Audio Modulation)
RECEIVER USED: Uniden BC355N Analog Scanner

DESCRIPTION:
I am submitting a formal report regarding persistent, unauthorized long-range voice communications. While this frequency spectrum is federally restricted to short-range, low-power consumer data or localized Part 15 devices, active human voice communications are being intercepted across an extensive geographic range.

The signal density is severe enough to cause passive intermodulation inside my residence, inducing an electrical audio current across household infrastructure and causing an unmodified AC motor to physically vibrate the audible speech into the room.

NARRATIVE / INTERCEPTED CONTENT SUMMARY:
[Brief factual summary of what voices are discussing.]

EVIDENCE:
I have chronological time logs and dual-source audio/video recordings verifying the audio heard on the frequency matches the physical acoustic bleed in real-time. Evidence is preserved and available for investigators.
```

### ICC Utility Complaint Template

```text
ILLINOIS COMMERCE COMMISSION — INFORMAL COMPLAINT
Utility: [ComEd / Ameren Illinois / MidAmerican Energy / Other]
Account Number: [Your account number]
Service Address: [Your address]
Reference: ICC 3086-2026

DESCRIPTION OF ISSUE:
I am experiencing persistent radio frequency interference (RFI) that I believe may be related to utility-owned power lines, transformers, smart meters, or grid infrastructure. The interference manifests as audible voice or audio bleeding through my household HVAC/AC motor chassis. I have documented the interference with a Uniden BC355N analog scanner and have isolated specific frequencies.

I am requesting a power quality investigation and an RF interference assessment by the utility's technical team. I have referenced IEEE 1897-2024 for power line gap interference source location procedures.

Chronological logs and synchronized dual-source audio/video recordings are available upon request.
```

---

## ⚖️ Regulatory & Law Enforcement Reporting

### Illinois / Federal Agency Directory

| Agency | Best Used For | Contact |
|---|---|---|
| **FCC Chicago Field Office** | Directional tracking vans, hunting transmitters, fines. | (847) 813-4672 / FCC Consumer Complaint Center |
| **Illinois Commerce Commission (ICC)** | Smart utility meter network bleed, grid equipment, utility complaints. | 1-800-524-0795 / Illinois Public Utility Portal |
| **FBI** | Illegal activity, threats, national security, intercepted communications. | 1-800-CALL-FBI / tips.fbi.gov |
| **APCO International** | Technical recording review, spectrum checking. | APCO Interference Management Center |
| **Illinois State Police TSB** | Emergency communication interference, public safety grid. | ISP Telecommunications Bureau Contact Directory |
| **Citizens Utility Board (CUB)** | Consumer advocacy, utility complaint assistance. | 800-669-5556 |

### Agency Detail

**1. The Federal Authority: FCC Chicago Field Office**
- Illinois falls under the FCC Chicago Regional Field Office.
- They record and process interference complaints on unlicensed bands.
- They deploy field agents with directional tracking vans.
- File electronically via the FCC Consumer Complaint Center (select the Radio icon).

**2. The State Authority: Illinois Commerce Commission (ICC)**
- Regulates public utilities and telecommunications networks.
- Monitors Advanced Metering Infrastructure (AMI) wireless networks in the 900 MHz spectrum.
- Contact: 1-800-524-0795 or the Illinois Public Utility Portal.
- **Reference:** ICC 3086-2026

**3. Emergency & Interoperability: Illinois State Police (ISP)**
- The ISP Telecommunications Services Bureau (TSB) manages statewide communications centers.
- Enforces the “Interference with Emergency Communication” statute.
- Contact via the ISP Telecommunications Bureau Contact Directory.

**4. Technical Frequency Coordinators: APCO International**
- Authorized spectrum manager.
- Reviews automated radio logs and processes technical reports.
- Contact via the APCO Interference Management Center.

**5. Consumer Advocacy: Citizens Utility Board (CUB)**
- Independent consumer advocacy organization for Illinois utility customers.
- Consumer Hotline: 800-669-5556
- Local: 312-263-4282
- Website: citizensutilityboard.org

### FCC Rule for 917.5000 MHz (Part 15)

- 902–928 MHz is an **unlicensed ISM band**.
- Part 15 devices must accept interference and must not cause harmful interference.
- Legal ERP limit: **4 W**.
- Long-range voice on 917.5 MHz suggests illegal amplification or malfunctioning equipment.
- FCC can dispatch mobile tracking vans and issue citations.

### FCC Rule for 937.0250 MHz

- **Outside** the 902–928 MHz ISM band.
- 928–960 MHz in the US includes fixed microwave, land mobile, utility SCADA, and certain Part 15 operations.
- If interference originates from a licensed service, the FCC coordinates with the license holder.
- If from an unlicensed device causing harmful interference, Part 15 rules apply.

### When to Report to FBI

- If intercepted audio involves threats, illegal activity, or national security concerns.
- If voices on **865.5000 MHz** sound like harassment or role-play.
- Provide frequency, location, time logs, and transcriptions.
- Do not confront suspected operators yourself.

### How to File a Complaint Against an Electric Utility

**Step 1: Contact the Utility Directly**
Before escalating, call the utility’s customer service line and report the issue. Ask for a **“power quality”** or **“RF interference”** investigation. Utilities employ **power quality teams** specifically focused on identifying and rectifying power quality issues quickly.

**Step 2: File an Informal Complaint With the ICC**
If the utility does not resolve the issue, file an informal complaint with the **Illinois Commerce Commission (ICC) Consumer Services Division**:

| Method | Contact |
|---|---|
| **Phone (toll-free)** | 1-800-524-0795 |
| **Phone (out-of-state)** | 1-217-782-2024 |
| **TTY** | 1-800-858-9277 |
| **Online** | ICC Consumer Services Portal |
| **Mail** | 527 East Capitol Ave, Springfield, IL 62701 |

**Step 3: File a Formal Complaint With the ICC**
If the informal complaint is not resolved, the ICC has jurisdiction over formal complaints alleging violations by utilities. A customer may submit a complaint by U.S. mail, facsimile, email, or telephone to the utility’s **Alternative Retail Electric Supplier (ARES)** or directly to the Commission.

**Step 4: Escalate to the FCC**
If the utility’s equipment is causing **harmful radio interference**, the FCC has authority to require utilities to remediate. The FCC has previously contacted utility companies (including ComEd and OG&E) to resolve power line noise complaints.

- **FCC Consumer Complaint Center:** File online under the Radio / Interference category.
- **FCC Chicago Field Office:** (847) 813-4672

**Step 5: Contact the Citizens Utility Board (CUB)**
The Citizens Utility Board is an independent consumer advocacy organization for Illinois utility customers:

| Contact | Detail |
|---|---|
| **Consumer Hotline** | 800-669-5556 |
| **Local** | 312-263-4282 |
| **Website** | citizensutilityboard.org |

---

## ⚡ Electric Utility Company Contact Directory

> [!NOTE]
> **Why electric companies are included:** Electric utility companies own and operate the power lines, transformers, meters, and grid infrastructure that can act as **accidental antennas** in passive RF rectification scenarios. If power-line hardware, smart meters, or utility-owned equipment is contributing to the interference, the utility must be contacted first before escalating to the FCC or ICC. The IEEE 1897-2024 standard specifically describes procedures that **electric utility companies** should use to address complaints of interference caused by power-line gap noise to radio, television, and other wireless communications.

### 🏢 Major Illinois Electric Utilities

| Utility | Service Area | Customer Service | Emergency / Outage | Business | Notes |
|---|---|---|---|---|---|
| **Commonwealth Edison (ComEd)** | Northern Illinois, Chicago metro | 1-800-334-7661 (1-800-EDISON-1) | 1-800-334-7661 | 1-877-426-6331 | Largest electric utility in Illinois; serves over 4 million customers. |
| **Ameren Illinois** | Central and Southern Illinois | 1-800-755-5000 | 1-800-755-5000 | 1-800-232-2477 | Investor-owned; serves central/southern IL. |
| **MidAmerican Energy** | Northern Illinois (Rock Island area) | 1-888-427-5632 | 1-800-799-4443 | 1-800-329-6261 | Serves IL, IA, SD; based in Des Moines. |
| **Mt. Carmel Public Utility** | Mt. Carmel, IL | Contact via ICC | — | — | Small investor-owned utility. |
| **McDonough Power Cooperative** | McDonough County area | Contact via ICC | — | — | Rural electric cooperative. |
| **Menard Electric Cooperative** | Menard County area | Contact via ICC | — | — | Rural electric cooperative. |
| **Corn Belt Energy Corporation** | Central Illinois | Contact via ICC | — | — | Rural electric cooperative. |
| **Jo-Carroll Energy** | Jo Daviess / Carroll counties | Contact via ICC | — | — | Rural electric cooperative. |

> [!TIP]
> **If you are unsure which utility serves your address**, check your most recent electric bill or use the Illinois Commerce Commission utility lookup.

### 📞 ComEd (Commonwealth Edison) — Detailed Contact

| Department | Contact | Notes |
|---|---|---|
| **Customer Service** | 1-800-334-7661 | 7 a.m. – 7 p.m., Mon–Fri. |
| **Emergency / Outage** | 1-800-334-7661 | 24/7 for downed lines, sparking, voltage problems. |
| **Business Services** | 1-877-426-6331 | Commercial accounts. |
| **Spanish Line** | 1-800-955-8237 | — |
| **FCC / RF Coordinator** | (630) 576-6886 | James Bortscheller, Exelon Corp. |
| **Email (FCC matters)** | fcc@exeloncorp.com | For formal RF interference correspondence. |
| **General Counsel** | E. Glenn Rippie — glenn.rippie@exeloncorp.com | SVP & General Counsel, ComEd. |

> [!NOTE]
> **Power Line Noise Reporting Procedure for ComEd:**
> 1. Identify the exact pole number on the pole nearest the noise source.
> 2. Record the pole number and location.
> 3. Call **1-800-334-7661** and report “static on my radio” along with the pole number.
> 4. ComEd field crews can locate and repair arcing hardware, loose connections, or failing arresters causing RF noise.

### 📞 Ameren Illinois — Detailed Contact

| Department | Contact | Notes |
|---|---|---|
| **Residential Customer Service** | 1-800-755-5000 | — |
| **Business Customer Service** | 1-800-232-2477 | — |
| **FCC / RF Coordinator** | (314) 554-2302 | Ameren Services Co. |
| **Email (FCC matters)** | fcc_coordinator@ameren.com | For formal RF interference correspondence. |
| **Ameren IL Service** | AmerenILSERVICE@ameren.com | General service email. |

> [!NOTE]
> **Ameren RF Interference Case Example:** In ICC Docket 24-0778 (Hank Bonnell vs. Ameren Illinois), a customer reported a buzzing noise in his house. Ameren was directed to perform a **frequency tech check** for interference that could be causing the issue.

### 📞 MidAmerican Energy — Detailed Contact

| Department | Contact | Notes |
|---|---|---|
| **Customer Service** | 1-888-427-5632 | Residential and business. |
| **Outage / Emergency** | 1-800-799-4443 | 24/7. |
| **Business Services** | 1-800-329-6261 | Commercial accounts. |
| **Illinois Regulatory Contact** | Mitchell Salek — mitchell.salek@midamerican.com | Rock Island, IL office. |
| **Regulatory Contact** | Jeffrey Cook — jeffrey.cook@midamerican.com | Des Moines, IA HQ. |

### 📡 Smart Meter & Grid Infrastructure RF Considerations

Modern electric utilities deploy **Advanced Metering Infrastructure (AMI)** — smart meters that communicate wirelessly in the 900 MHz spectrum. These devices are network elements that transmit meter data plus alarms, flags, and events to routers and repeaters.

#### Relevant Bands for Utility Infrastructure

| Band | Use | Relevance to This Investigation |
|---|---|---|
| **902–928 MHz ISM** | Smart meters, LoRaWAN, AMI mesh networks | **917.5000 MHz** falls here. Smart meters are a potential source of digital data bursts, though they normally do not transmit voice. |
| **928–960 MHz** | Fixed microwave, land mobile, utility SCADA | **937.0250 MHz** falls here. Utility SCADA and licensed land mobile systems may operate in this range. |

#### If You Suspect Smart Meter Interference

1. **Contact your utility’s power quality team** and request a meter and service panel inspection.
2. **Document the exact times** the interference occurs and whether it correlates with meter reading cycles.
3. **File an ICC complaint** if the utility does not respond adequately.
4. **Note:** Smart meters transmit **digital data packets**, not analog voice. If you hear clear human speech, the source is more likely a different transmitter — but the utility’s wiring and infrastructure may still be acting as the accidental antenna that is **receiving and demodulating** that signal.

#### Smart Meter Complaints in Illinois

Consumer complaints regarding smart meters increased **54 percent** in the first 10 months of 2025 compared to all of 2024, triggering an ICC investigation. Multiple ICC dockets address smart meter installation, damage, and interference concerns.

### 🔧 Power Line Noise & RF Interference — Technical Background

Electric utility infrastructure can generate RF noise through:

| Source | Mechanism | Frequency Range |
|---|---|---|
| **Arcing insulators** | Corona discharge at damaged insulators | Broadband, often 1–30 MHz |
| **Loose hardware** | Micro-arcing at bolts, clamps, and connectors | Broadband |
| **Failing arresters** | Internal degradation causes partial discharge | Can be ultrasonic + RF |
| **Smart meters / AMI** | Digital data transmission | 902–928 MHz |
| **SCADA / telemetry** | Licensed land mobile and microwave | 928–960 MHz, higher bands |

#### IEEE 1897-2024 Standard

The IEEE Recommended Practice for Location of Power Line Gap Interference Sources describes procedures that **electric utility companies** may use to address complaints of interference caused by power-line gap noise. It includes methods to determine if noise is **harmful interference** under FCC rules, and techniques such as **time-domain noise signatures** (signature analysis) to investigate and identify radio noise in the field.

> **This means:** Utilities have a documented, standardized process for investigating your complaint. When you contact them, you can reference **IEEE 1897-2024** to signal that you expect a professional investigation.

---

## 🛠️ Physical Mitigation

### Ferrite Chokes

- Purchase **snap-on RFI/EMI ferrite core beads** sized 10 mm or 13 mm.
- Snap onto main power lines entering the AC motor casing.
- Ferrites allow 60 Hz power through but choke high-frequency RF.
- Converts RF to harmless heat.

### Grounding

- Inspect the green/bare copper ground wire bonding HVAC frame to electrical panel.
- Clean rust/oxidation.
- Tighten grounding screws.
- Low-resistance ground drains stray RF into earth.

### Other Mitigation

- Use shielded cables.
- Cross power and audio wires at 90°.
- Isolate audio power with conditioner.
- Keep audio gear away from motors.

```mermaid
flowchart LR
    A[Incoming Unshielded Line] --> B[Ferrite Core Bead]
    B --> C[AC Motor Windings]
    C --> D[Reduced RF Audio Bleed]
```

```html
<!-- SYSTEM FILTRATION SCHEMATIC: WIRE-LEVEL ISOLATION -->
<p align="center">
  <b>[Incoming Unshielded Line]</b> ───► █ Ferrite Core Bead █ ───► <b>[AC Motor Winds Core]</b>
</p>
```

---

## 🤖 AI Research Prompt

Copy and paste this into an AI tool for further analysis.

```text
Act as an expert in RF engineering, telecommunications compliance, and radio frequency interference (RFI) diagnostic troubleshooting. I need you to analyze a highly specific passive radio frequency interference issue occurring in my immediate environment and serve as my step-by-step consulting companion for resolving it.

CONTEXT AND ENVIRONMENT DATA:
1. Target System: An unmodified household electric AC motor and HVAC system. The unit has no built-in audio system, communication hardware, or modifications.
2. The Phenomenon: I am standing directly next to this completely stock AC motor and am hearing legible, distinct human voices and audio broadcasts emitting physically from the machine chassis. I have ruled out mental pattern recognition (auditory pareidolia) because the sound waves are acoustic, localized to the machine, and can be recorded using standard mobile microphone hardware.
3. Isolated Frequencies: Using a Uniden BC355N analog base/mobile scanner placed directly next to the machine, I captured signals at 917.5000 MHz, 865.5000 MHz, and 937.0250 MHz. A 462.8875 MHz reading was a baseline scan capture, not a confirmed target.
4. Transmitter Profile: 917.5000 MHz is in the 902-928 MHz ISM band, usually digital data. Analog voice could be older cordless phone, wireless mic, baby monitor, or illegally amplified Part 15 device. 865.5000 MHz and 937.0250 MHz are not fully decoded.

SCIENTIFIC PRINCIPLE:
Treat this as a possible case of Passive Intermodulation (PIM) / "Rusty Bolt" effect. The HVAC metal acts as an accidental resonant antenna. A corroded or loose metal junction acts as a crude metal-oxide diode. This rectifies the RF carrier, passing audio current into the AC motor windings. The motor's stator plates vibrate, acting as a speaker.

YOUR CAPABILITIES AND TASKS:
1. COMPLIANCE ASSISTANCE: Help draft FCC, ICC, FBI, APCO, and electric utility reports.
2. ADVANCED RECORDING LOGISTICS: Provide instructions for dual-source synchronized audio/video evidence.
3. MOTOR HARDWARE TROUBLESHOOTING: Outline ferrite choke and grounding mitigation.
4. UNIDEN BC355N MANUAL SEQUENCE HELP: Guide Squelch, Private memory, Close Call Only, Lockout, and Master Reset.

Acknowledge the physical constraints, the logged frequencies, the Uniden BC355N, and the Rusty Bolt diode rectification phenomenon. Await my direction.
```

---

## 📎 Appendices

### Glossary

| Term | Definition |
|---|---|
| **PIM** | Passive Intermodulation — unwanted signal mixing in passive components. |
| **Rusty Bolt Effect** | Corroded metal junction acting as a diode, demodulating RF. |
| **Transduction** | Conversion of one energy form to another. |
| **Pareidolia** | Brain perceiving meaningful patterns in random noise. |
| **Close Call** | Uniden feature that locks onto strong nearby RF signals. |
| **Squelch** | Gate that mutes static when no signal is present. |
| **Ferrite Choke** | Magnetic bead that suppresses high-frequency RF on cables. |
| **Part 15** | FCC rules for unlicensed low-power devices. |
| **ISM Band** | Industrial, Scientific, Medical unlicensed spectrum. |
| **ERP** | Effective Radiated Power. |
| **GMRS** | General Mobile Radio Service. |
| **APCO** | Association of Public-Safety Communications Officials. |
| **TSB** | Telecommunications Services Bureau (Illinois State Police). |
| **ICC** | Illinois Commerce Commission. |
| **CUB** | Citizens Utility Board. |
| **AMI** | Advanced Metering Infrastructure (smart meters). |
| **SCADA** | Supervisory Control and Data Acquisition (utility grid control). |

### FAQ

**Q: Can an unmodified motor miles away transmit audio?**
A: No. Physics rules out efficient audio transmission over miles from an unmodified motor.

**Q: Can a motor right next to me play audio?**
A: Yes, rarely, via PIM/Rusty Bolt or as pareidolia.

**Q: Can a normal person hear this?**
A: Yes. Both physical RF demodulation and pareidolia are universal human experiences.

**Q: Does the BC355N cover 917.5000 MHz?**
A: Yes. Coverage is 25–956 MHz.

**Q: Does the BC355N cover 937.0250 MHz?**
A: Yes. It is within the 806–956 MHz coverage block.

**Q: Does the BC355N cover AM broadcast 530–1700 kHz?**
A: No. Use a separate portable AM radio.

**Q: Is 462.8875 MHz the target?**
A: No. It was a baseline scan capture. The confirmed target observations are 917.5000 MHz, 865.5000 MHz, and 937.0250 MHz.

**Q: Can ferrite chokes stop the voices?**
A: They can reduce RF coupling into the motor. Results vary.

**Q: Is the BC355N AC or DC powered?**
A: It is powered by **13.8 V DC**. Home use requires an AC-to-DC adapter; vehicle use requires a DC cigarette lighter cord.

**Q: What should I do if I hear harassment or role-play on 865.5000 MHz?**
A: Report it to the FCC, FBI, and other agencies listed in [Regulatory & Law Enforcement Reporting](#-regulatory--law-enforcement-reporting). Do not confront the operators.

**Q: Why are electric companies included in this repo?**
A: Electric utility companies own the power lines, transformers, meters, and grid infrastructure that can act as accidental antennas in passive RF rectification. They must be contacted first before escalating to the FCC or ICC. The IEEE 1897-2024 standard describes procedures utilities should use to address power-line gap interference complaints.

**Q: How do I contact my electric utility about RF interference?**
A: Call the utility’s customer service line, ask for a “power quality” or “RF interference” investigation, provide account number, service address, pole number, and a chronological log. If unresolved, file an ICC complaint.

**Q: What is IEEE 1897-2024?**
A: The IEEE Recommended Practice for Location of Power Line Gap Interference Sources. It describes procedures electric utility companies may use to address complaints of interference caused by power-line gap noise.

### Repository Structure

```text
ELECTROMAGNETIC-AUDIO-TRANSDUCTION/
├── README.md
├── docs/
│   ├── science.md
│   ├── rusty-bolt.md
│   ├── scanner-bc355n.md
│   ├── evidence-protocol.md
│   ├── reporting-illinois.md
│   └── electric-utilities.md
├── logs/
│   ├── observation-log.csv
│   └── timeline.md
├── templates/
│   ├── fcc-complaint.txt
│   ├── fbi-tip.txt
│   ├── icc-inquiry.txt
│   └── utility-complaint.txt
└── media/
    ├── dual-source-video-guide.md
    └── ferrite-mitigation.md
```

### Key Reference Links

- SparkFun: What is Electricity?
- Wikipedia: Atmospheric electricity
- UCAR SciEd: Atmospheric Electricity Movie
- Ion Power Group: How It Works on Earth
- Quora: Are there electric fields present everywhere?
- Ansys: What is Crosstalk?
- QSC: What Causes Loudspeaker Hum and Hiss?
- Accustic Arts: How Electrical Interference Affects Audio
- ALLPCB: How AC Motor EMI Occurs
- Rohm: Crosstalk in Circuit Design
- ProSoundWeb: AC Power Coupling Into Audio Signal Cables
- FCC: Interference Resolution
- FCC: Amateur Radio Complaints
- FCC: Consumer Complaint Center
- Uniden: BC355N Product Page
- RadioReference Wiki: BC-355N
- APCO: Interference Reporting
- Illinois Commerce Commission: Consumer Services
- FBI: Tips
- IEEE 1897-2024: Recommended Practice for Location of Power Line Gap Interference Sources
- Citizens Utility Board: citizensutilityboard.org

---



> **Final Note:** This repository is a living document. Append new observations chronologically. Do not alter historical entries. Verify frequencies before reporting. When in doubt, consult a licensed electrician, RF engineer, or attorney.
