# CanSat — Atmospheric Data Acquisition

My team and I built a CanSat prototype to integrate atmospheric sensing,
onboard electronics and wireless telemetry in a compact payload. The project
record describes a 700-gram assembly. This repository currently preserves the
project description and prototype photographs; it does not contain firmware,
schematics or a reproducible flight-test dataset.

## System architecture

```text
IMU / environmental sensors → microcontroller → Zigbee radio → ground station
                                  ↑
                         battery / power subsystem
```

This is a conceptual summary of the documented design, not an as-built wiring
diagram. Exact part numbers, sampling rates and power ratings remain unrecorded here.

## Hardware and sensing

The documented subsystems are a microcontroller, Zigbee communication modules,
IMU/gyroscope and environmental sensors, battery management and the mechanical
payload assembly. Eagle CAD and C/C++ are listed in the original project account;
the corresponding CAD and firmware files have not been recovered for this repository.

## Communications and embedded software

The intended data path acquired orientation and environmental readings onboard
and transmitted telemetry to a ground station. No packet specification, ground-
station code, sample telemetry or range-test log is retained here. I do not claim
a verified 1 km link, autonomous power performance or a measured data-loss rate.

## My contributions and the team's work

My recorded contributions were hardware/software integration, the Zigbee link,
sensor acquisition programming and assistance with the power subsystem. The team
collectively built and integrated the payload. This summary follows the original
project account; individual commits, schematics and subsystem test records are
not available to independently apportion every task.

## Testing and measured results

The original account reports deployment, descent and recovery. The photographs
are qualitative project evidence, not calibrated flight or reliability records.
No telemetry trace, altitude history, environmental calibration, measured power
budget or launch/recovery test report is committed. Accordingly, launch survival,
range and sensing accuracy are not established as measured results here.

## Prototype photographs

<p align="center">
  <img src="https://github.com/user-attachments/assets/b51c912b-054a-4a3d-8e1e-58402c0ffcac" 
       alt="CanSat Deployment Test" 
       width="800"/>
</p>

<table align="center">
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/64056ccb-02ab-4f83-be84-5a9475482522" 
           alt="CanSat Prototype - Internal View" width="400"/><br>
      <sub><b>Internal View</b></sub>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/daa2a602-0220-48ed-9eaf-87395547ac8a" 
           alt="CanSat Prototype - External View" width="400"/><br>
      <sub><b>External View</b></sub>
    </td>
  </tr>
</table>


The images retain their existing GitHub attachment URLs and captions. Their
availability and team-media redistribution scope should be confirmed before
reuse elsewhere; no new image or flight evidence was created for this revision.

## Missing evidence and acknowledgments

- Recover the as-built bill of materials, wiring and Eagle CAD with team permission.
- Recover authentic firmware, ground-station source and communication framing.
- Add calibration/range/power tests and timestamped telemetry if retained.
- Separate measured launch/descent/recovery outcomes from intended capabilities.
- Credit the team and establish rights for every additional file.

This was a team hardware project. It remains public as an engineering record;
stronger technical evidence is needed before featuring it as a measured-performance
project. The existing license is unchanged and does not establish rights to
additional team material.
