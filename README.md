flowchart TD
  subgraph Evidence
    EV1[Información del servicio] --> EV2[Formulario de ingreso]
  end

  subgraph Customer Journey
    A[Usuario ingresa datos en formulario] --> B[Validación automática de datos]
    B --> C[Verifica Ubicación del vehículo]
    C --> D[Consulta aseguradora]
  end

  subgraph Frontstage
    D --> E[Obtiene datos de la aseguradora]
    E --> F[Calcula kilómetros mediante fórmulas]
    F --> G[Aplica tarifas preconfiguradas]
  end

  subgraph Backstage Actions
    G --> H[Generación automática de factura]
    H --> I[Envío automático de factura]
  end

  subgraph Support Processes
    I --> J[Almacenamiento en sistema]
    J --> K[Envío de mensaje a conductores de grúas]
    K --> L[Proceso finalizado]
  end

  classDef evidence fill:#E3F2FD,stroke:#000
  classDef customerJourney fill:#BBDEFB,stroke:#000
  classDef frontstage fill:#90CAF9,stroke:#000
  classDef backstage fill:#64B5F6,stroke:#000
  classDef support fill:#42A5F5,stroke:#000

  class EV1,EV2 evidence
  class A,B,C,D customerJourney
  class E,F,G frontstage
  class H,I backstage
  class J,K,L support
