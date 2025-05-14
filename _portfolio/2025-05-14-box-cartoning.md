---
title: Autonomous Box Cartoning Machine
header:
  video:
    id: 1nnGwnFD8Xu8tv5LKCi4SV5Wn84-GdKqO
    provider: google-drive
cad:
  - url: /assets/images/box-erector/CAD/first-design.png
    image_path: /assets/images/box-erector/CAD/first-design.png
    alt: "First CAD design"
    title: "Initial CAD Layout"

  - url: /assets/images/box-erector/CAD/AStudio-model.png
    image_path: /assets/images/box-erector/CAD/AStudio-model.png
    alt: "Automation Studio diagram"
    title: "Pneumatic Control Simulation in Automation Studio"

  - url: /assets/images/box-erector/CAD/final-model.png
    image_path: /assets/images/box-erector/CAD/final-model.png
    alt: "Final model"
    title: "Final Assembly"

  - url: /assets/images/box-erector/CAD/final-model2.png
    image_path: /assets/images/box-erector/CAD/final-model2.png
    alt: "Alternate final model"
    title: "Alternate View"

diagrams:
  - url: /assets/images/box-erector/Diagrams/wiring-diagram1.png
    image_path: /assets/images/box-erector/Diagrams/wiring-diagram1.png
    alt: "system block diagram"
    title: "Wiring block diagram showing all components"

  - url: /assets/images/box-erector/Diagrams/wiring-diagram2.png
    image_path: /assets/images/box-erector/Diagrams/wiring-diagram2.png
    alt: "Limit switch wiring diagram"
    title: "Limit switch wiring diagram"

  - url: /assets/images/box-erector/Diagrams/wiring-diagram3.png
    image_path: /assets/images/box-erector/Diagrams/wiring-diagram3.png
    alt: "Relay/solenoid valve wiring diagrm"
    title: "Relay/DCV wiring diagram"

  - url: assets\images\box-erector\Diagrams\wiring-diagram-servo.png
    image_path: assets\images\box-erector\Diagrams\wiring-diagram-servo.png
    alt: "Servo motor wiring diagram"
    title: "Servo motor wiring diagram (identical for each motor)"

pics:
  - url: assets\images\box-erector\pics\basic-wiring.png
    image_path: assets\images\box-erector\pics\basic-wiring.png
  
  - url: assets\images\box-erector\pics\initial-mounting.png
    image_path: assets\images\box-erector\pics\initial-mounting.png
  
  - url: assets\images\box-erector\pics\top-labelled.png
    image_path: assets\images\box-erector\pics\top-labelled.png

published: true
---

Year 2 capstone project showcasing the design and development of an autonomous box cartoning machine using embedded firmware, pneumatics, and custom wiring. Includes CAD models, wiring diagrams, and final build photos.

# Development

{% include gallery id="pics" caption="System at various stages of development"%}


# CAD Models

{% include gallery id="cad" %}

# Diagrams 

{% include gallery id="diagrams" %}

# Control Flow

{% include figure popup=true image_path="assets\images\box-erector\Diagrams\flowchart.png" alt="control flow chart" %}
