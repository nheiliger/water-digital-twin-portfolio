# water-digital-twin-portfolio

# Water Treatment Digital Twin Portfolio  
Real-scale, cyber-physical digital twins of drinking water & wastewater plants  
Built 2025–2026 | AWS • NVIDIA Omniverse • OpenPLC • MiniCPS • Caldera

Live demos:  
Mini-SWaT Twin → https://your-scene-link  
Municipal Plant Twin → https://your-grafana-playground  
Cyber Attack Demo → YouTube (coming)

Actively hiring / consulting offers welcome → linkedin.com/in/yourname
water-digital-twin-portfolio/                  ← Main repo (public, great README)
│
├── README.md                                  ← Your “front door” (update as you go)
├── LICENSE                                    ← MIT License
├── .github/
│   └── workflows/ci.yml                       ← Optional GitHub Actions for auto-tests
│
├── 01-mini-swat-twin/                         ← Project 1 – SWaT replica
│   ├── docs/
│   │   ├── SWaT_Process_Description.pdf       ← Official iTrust diagram + your annotations
│   │   ├── Dataset_2015_2019_Description.md
│   │   └── Attack_List_36.md                  ← Table of all 36 real attacks you replay
│   ├── plc-code/                              ← OpenPLC / Ladder logic
│   │   ├── P1-P6_All_Stages.xml               ← Exact SWaT logic (publicly shared by iTrust)
│   │   └── custom_mods/                       ← Your small improvements
│   ├── simulation/
│   │   ├── minicps-swat/                      ← MiniCPS real-time simulation
│   │   └── epanet-distribution/               ← Optional distribution extension
│   ├── aws-iot-twinmaker/
│   │   ├── component-types/                   ← DTDL/GraphQL models for each sensor/actuator
│   │   ├── scenes/                            ← TwinMaker Scene Composer files
│   │   └── dashboard/                         ← Grafana JSON dashboards
│   ├── omniverse-viewer/
│   │   ├── usd/                               ← 3D SWaT plant (converted from original STEP files)
│   │   └── extensions/                        ← Live data connector to AWS
│   ├── data/
│   │   ├── 2015-2019_datasets/                ← Raw CSV (link to iTrust, don’t host full 50 GB)
│   │   └── synthetic/                         ← Your generated data when needed
│   ├── attacks/
│   │   └── caldera-playbooks/                 ← 36 YAML attack playbooks
│   └── demo-video/                            ← 5-minute YouTube unlisted link embedded in README
│
├── 02-municipal-plant-twin/                   ← Project 2 – Real-scale plant
│   ├── 3d-assets/
│   │   ├── raw/                               ← Original Revit/IFC from public plants
│   │   └── usd/                               ← Clean OpenUSD versions
│   ├── omniverse-blueprint/
│   │   ├── water-treatment-factory/           ← Modified Industrial Facility blueprint
│   │   └── flow-simulations/                  ← Chlorine contactor + UF membrane physics
│   ├── aws-deployment/
│   │   ├── terraform/                         ← IaC for 800+ assets
│   │   └── timestream-queries/
│   ├── ml-models/
│   │   └── pump-failure-prediction/           ← SageMaker notebook
│   └── dashboard/                             ← Public Grafana playground link
│
├── 03-cyber-physical-defense-twin/            ← Project 3 – Red/Blue demo
│   ├── caldera-water-profile/
│   │   └── abilities/                         ← Custom water-specific TTPs
│   ├── detection/
│   │   ├── sagemaker-anomaly-model/
│   │   └── guardduty-rules/
│   └── report/
│       └── Water_Digital_Twin_Cyber_Attack_Report.pdf  ← 15-page whitepaper
│
├── presentations/
│   ├── AWWA_ACE_2026_Poster.pdf
│   ├── Singapore_Water_Week_2026.key
│   └── 5-minute-lightning-talk.mp4
│
└── professional/
    ├── Digital_Twin_Water_Capability_Statement.pdf   ← 2-pager for utilities
    └── resume-water-digital-twin.pdf
