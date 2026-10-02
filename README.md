# Data Centre Electrical Design

Electrical design of a **1 MW (IT load) data centre** with a **2N architecture**: two fully independent power paths (A and B), each able to carry the whole facility on its own.

The project shows how a design goes from a defined scenario to sized equipment, a single line diagram, fault and protection studies, and a reliability estimate.

> **Status:** Preliminary design for academic project use. Not for construction.

## Repository structure

```
Data-Centre-Electrical-Design/
├── report/
│   └── DC_Electrical_Design_Report.docx    Full design report
├── calculations/
│   └── DC_Electrical_Design_Calcs.xlsx     All calculations (live formulas)
└── diagrams/
    ├── DC_SLD_2N.png                       Single line diagram
    └── DC_Protection_TCC.png               Time-current coordination curves
```

## Design basis

| Parameter | Value |
| --- | --- |
| Racks x average load | 200 x 5 kW |
| IT load | 1,000 kW |
| Total facility load | 1,500 kW (PUE 1.50) |
| Redundancy | 2N, each path sized for 100% of load |
| Utility supply | 11 kV, assumed 250 MVA fault level |
| LV system | 415 V, 3-phase, 50 Hz, TN-S |
| Growth margin | 20% |
| Design ambient | 45 °C |
| Battery / fuel autonomy | 10 min / 24 h |

## Key results (per path)

| Item | Selected |
| --- | --- |
| Transformer | 2,500 kVA, 11/0.415 kV |
| UPS | 1,200 kVA double conversion |
| Battery | 4 x 300 Ah at 480 V (576 kWh) |
| Generator | 2,500 kVA / 2,000 kW, 9,720 L tank |
| PDUs | 4 x 400 kVA |
| Max LV fault level | 51.2 kA (65 kA rated equipment) |

**Reliability:** estimated availability of 99.99917% for 2N (about 4.4 min/year), compared with 99.92304% for a single path. These figures use illustrative component data and are meant for comparing configurations, not as a guarantee.

## What the report covers

1. Introduction and scope
2. Design basis
3. Load calculation
4. Architecture and single line diagram
5. Equipment sizing (transformer, UPS, battery, generator, PDU/RPP)
6. Cable sizing and voltage drop
7. Short-circuit calculation
8. Protection and coordination
9. Reliability and availability
10. Failure scenarios
11. Equipment list
12. Assumptions, limitations and verification

**Not included:** cooling design, civil and structural work, fire suppression, BMS/DCIM, harmonic study, arc-flash study, cost estimation.

## Reference standards

TIA-942 and Uptime Institute guidance, IEC 60364, IS 732, IEC 62040-3, IS 2026, IEC 60909, IEC 60947-2, ISO 8528, IS 3043, IEC 61643, IEEE 493.

## Limitations

The utility fault level and reliability data are assumptions and must be replaced with real data before any detailed design. The battery sizing is an energy-based estimate and needs checking against manufacturer discharge tables.

## Author

Mohit

## License

MIT, see [LICENSE](LICENSE).
