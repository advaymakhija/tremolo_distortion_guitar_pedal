# 🎸 Analog Guitar Pedal Chain: Distortion + Tremolo

This project is a custom-built **analog guitar effects chain** consisting of two core circuits: a **Distortion Pedal** and a **Tremolo Pedal**, connected through a **buffer stage**. The system is designed for modularity and flexibility, allowing you to generate rich tonal textures in real time using analog circuitry.

---

## 🔧 Overview

- 🎛️ **Distortion Circuit**: Achieved using an **amplifier** followed by a **clipper stage** (typically using diodes) to introduce soft/hard clipping and distortion.
- 🌊 **Tremolo Circuit**: Built using a **BJT transistor** where a **sine wave** is applied to the base, modulating the amplitude of the input signal.
    - The sine wave can be generated via a **function generator** or a simple **oscillator circuit**.
    - Alternative waveforms (triangle, square) may be used to create different tremolo effects.

---

## 🧩 Circuit Breakdown

### 1. **Distortion Pedal**
- **Stage 1**: Amplification using an op-amp or discrete transistor amp.
- **Stage 2**: Clipping using diodes (e.g., 1N4148 or LEDs) to distort the amplified signal.

### 2. **Tremolo Pedal**
- **Modulation**: A BJT transistor acts as a variable resistor.
- **Control**: A low-frequency **sine wave** is applied to the **base** to modulate the gain, resulting in a volume pulsing effect.

---

## 🔁 Signal Chain and Buffering
- Guitar Input --> Distortion Circuit --> Buffer --> Tremolo Circuit --> Output Jack
- A **buffer** is placed between the distortion and tremolo stages to prevent loading issues and preserve tone integrity.
- Use a **unity gain op-amp buffer** (like a voltage follower) for optimal results.

---

## 🎚️ Assembly Instructions

1. **Build the Distortion Circuit**
    - Assemble amplifier + clipper on a breadboard or PCB.
    - Connect input jack to the amplifier input.
  
2. **Build the Tremolo Circuit**
    - Assemble BJT + sine wave input circuit.
    - You can use:
        - An external function generator
        - A small op-amp based sine wave oscillator
        - A microcontroller-based DAC if desired

3. **Add a Buffer Between the Two Circuits**
    - A simple op-amp voltage follower works.
    - Connect output of distortion → buffer → input of tremolo.

4. **Wire Up the Audio I/O**
    - Use 6.35mm mono jacks (standard guitar jacks)
    - **Input Jack**: Connect to distortion input
    - **Output Jack**: Connect to tremolo output

5. **Power**
    - Power the circuits using a 9V battery or a regulated supply
    - Use decoupling capacitors and ground plane if designing a PCB
