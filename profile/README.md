<p align="center"><img src="banner.png" alt="CorteX ARM — Brainwaves into action" width="100%"></p>

# CorteX ARM

**CorteX ARM** by team ArmExecuTorchEEG: real-time motor-imagery EEG decoding (left vs right hand) on the Alif Ensemble E8 (Cortex-M55 + Ethos-U85) with ExecuTorch. Built for the [Arm + ExecuTorch: Edge AI Challenge](https://arm-executorch.devpost.com/), San Francisco State University, October 17–18, 2026.

<p align="center"><picture>
<source media="(prefers-color-scheme: dark)" srcset="pipeline-dark.svg">
<img src="pipeline.svg" alt="System architecture: BCI IV 2a replay and host bridge on the laptop, UART into the Alif E8, preprocessing on the Cortex-M55, TinyEEGNet-wide int8 on the Ethos-U85, IMU motion gate, LEDs and JSON out to the demo UI" width="900">
</picture><br><sub>System architecture. Details, demo video and results: <a href="https://github.com/ArmExecuTorchEEG/CorteX-ARM">CorteX-ARM</a>.</sub></p>

**Start here: [CorteX-ARM](https://github.com/ArmExecuTorchEEG/CorteX-ARM)**, the submission: firmware, ML training code, demo UI, results and build instructions. Judged release: [`v1.0-submission`](https://github.com/ArmExecuTorchEEG/CorteX-ARM/releases/tag/v1.0-submission).

| | |
|---|---|
| Hardware | Alif Ensemble E8 DevKit: Cortex-M55 400 MHz + Ethos-U85 NPU, on-board IMU |
| Model | TinyEEGNet-wide, 3,426 parameters, 11.4 KB int8 `.pte`, all compute on the NPU |
| Accuracy | 77.1 % on the physical E8 (70 trials); 74.6 % int8 over all 9 BCI IV 2a subjects |
| Speed | 0.32 ms per inference on the Ethos-U85 (Corstone-320 FVP) |

## Team

| Name | Role |
|---|---|
| Moamen Soliman | EEG Model Architecture, Training & Optimization |
| Philippine Chauvet | Embedded AI Engineering, Firmware & Hardware Integration |
| Jihyung Ku | Frontend Engineering & UI/UX Design |
