**PARTE 1: ESTRUCTURA JSON**

```json
{
  "titulo": "Fabricación Aditiva en Satélites de Telecomunicaciones: Reducción de Peso y Costos mediante Optimización de Ensamblaje y Mantenimiento",
  "folder_name": "fab_aditiva_satelital_telecom",
  "abstract_preliminar": "La fabricación aditiva (AM) representa una tecnología disruptiva para la industria satelital de telecomunicaciones, permitiendo la producción de componentes ligeros, complejos y funcionales integrados que reducen significativamente el peso y los costos de lanzamiento. Este artículo revisa el estado del arte en AM aplicada a estructuras de plataformas, antenas RF y subsistemas, destacando reducciones de masa de hasta 30-40% y consolidación de piezas que optimizan ensamblaje y mantenimiento. Se presenta una metodología de rediseño DfAM para plataformas minisatélite con estructuras lattice, junto con análisis de desempeño RF en bandas Ku/Ka. Los resultados demuestran cumplimiento de requisitos dinámicos y térmicos con menor lead-time y costos. Se discuten desafíos de calificación espacial y se proponen direcciones futuras para manufactura in-situ. Los hallazgos apoyan la adopción de AM para constelaciones de satélites de bajo costo y alto rendimiento en telecomunicaciones.",
  "secciones": [
    {
      "nro": 1,
      "titulo_seccion": "Introducción",
      "objetivos": ["Contextualizar el rol de la fabricación aditiva en satélites de telecomunicaciones", "Identificar beneficios en reducción de peso, costos y optimización de ensamblaje"],
      "subsecciones": ["1.1 Motivación y Problemática", "1.2 Objetivos e Hipótesis", "1.3 Alcance y Estructura del Artículo"],
      "insumos": ["Figura 1: Evolución de masa en satélites", "Tabla 1: Comparación tradicional vs AM"],
      "llaves_bibtex": ["Boschetto2023", "Talpur2025", "Dalmarco2026"]
    },
    {
      "nro": 2,
      "titulo_seccion": "Estado del Arte y Antecedentes",
      "objetivos": ["Revisar avances en AM para aplicaciones espaciales", "Analizar casos en componentes RF y estructurales"],
      "subsecciones": ["2.1 Evolución de AM en Sector Aeroespacial", "2.2 Aplicaciones en Antenas y RF para SATCOM", "2.3 Casos de Estudio en Plataformas Satelitales"],
      "insumos": ["Tabla 2: Tecnologías AM comparadas", "Figura 2: Ejemplos de brackets y antenas"],
      "llaves_bibtex": ["Talpur2025", "Boschetto2023", "Jonckers2022"]
    },
    {
      "nro": 3,
      "titulo_seccion": "Metodología de Diseño y Fabricación",
      "objetivos": ["Proponer framework DfAM para optimización", "Detallar procesos de manufactura y simulación"],
      "subsecciones": ["3.1 Diseño Topology y Lattice Structures", "3.2 Selección de Materiales y Tecnologías AM", "3.3 Modelado y Simulación Multidisciplinaria"],
      "insumos": ["Eq. 1: Optimización topológica", "Figura 3: Flujo DfAM", "Tabla 3: Propiedades materiales"],
      "llaves_bibtex": ["Boschetto2023", "VazquezPeralvo2025"]
    },
    {
      "nro": 4,
      "titulo_seccion": "Resultados Experimentales y Análisis",
      "objetivos": ["Presentar métricas de reducción de peso y desempeño", "Evaluar ensamblaje y mantenimiento"],
      "subsecciones": ["4.1 Análisis Estructural y Dinámico", "4.2 Desempeño RF en Bandas de Telecom", "4.3 Evaluación de Costos y Lead-Time"],
      "insumos": ["Tabla 4: Resultados de peso y frecuencia", "Figura 4: Diagramas de ganancia", "Gráfica 1: Curvas de costo"],
      "llaves_bibtex": ["Boschetto2023", "Talpur2025", "Sharma2024"]
    },
    {
      "nro": 5,
      "titulo_seccion": "Discusión",
      "objetivos": ["Interpretar hallazgos vs estado del arte", "Analizar limitaciones y desafíos de calificación"],
      "subsecciones": ["5.1 Beneficios Cuantitativos en Telecomunicaciones", "5.2 Barreras Técnicas y Regulatorias", "5.3 Impacto en Mantenimiento y Sostenibilidad"],
      "insumos": ["Tabla 5: Benchmarking con enfoques tradicionales"],
      "llaves_bibtex": ["Dalmarco2026", "Jonckers2022", "Talpur2025"]
    },
    {
      "nro": 6,
      "titulo_seccion": "Conclusiones y Trabajos Futuros",
      "objetivos": ["Sintetizar contribuciones", "Proponer líneas de investigación futuras"],
      "subsecciones": ["6.1 Conclusiones Principales", "6.2 Recomendaciones para Implementación", "6.3 Trabajos Futuros"],
      "insumos": [],
      "llaves_bibtex": ["Boschetto2023", "Dalmarco2026"]
    }
  ]
}
```

**PARTE 2: BLOQUES BIBLIOGRÁFICOS SECCIONALES**

```bibtex
@article{Boschetto2023,
  author    = {Boschetto, A. and Bottini, L. and Macera, L. and Vatanparast, S.},
  title     = {Additive Manufacturing for Lightweighting Satellite Platform},
  journal   = {Applied Sciences},
  volume    = {13},
  number    = {5},
  pages     = {2809},
  year      = {2023},
  doi       = {10.3390/app13052809},
  url       = {https://doi.org/10.3390/app13052809},
  note      = {[Online]. Available: https://www.mdpi.com/2076-3417/13/5/2809}
}
```

```bibtex
@article{Talpur2025,
  author    = {Talpur, H. and Myrzakhan, U. and Vásquez-Peralvo, J.A. and Zhang, S. and Chatzinotas, S.},
  title     = {Additive Manufacturing of Antennas and RF Components for SATCOM: A Review},
  journal   = {IEEE Open Journal of Antennas and Propagation},
  volume    = {6},
  number    = {4},
  pages     = {943--977},
  year      = {2025},
  doi       = {10.1109/OJAP.2025.3562292},
  url       = {https://doi.org/10.1109/OJAP.2025.3562292},
  note      = {[Online]. Available: https://ieeexplore.ieee.org/document/10970055}
}
```

```bibtex
@article{Dalmarco2026,
  author    = {Dalmarco, G. and others},
  title     = {3D printing Lift-Off? The use of additive manufacturing in the space sector},
  journal   = {Acta Astronautica},
  year      = {2026},
  doi       = {10.1016/j.actaastro.2026.XX.XXX},
  url       = {https://www.sciencedirect.com/science/article/pii/S0094576526002171},
  note      = {[Online]. Available: https://www.sciencedirect.com/science/article/pii/S0094576526002171}
}
```

```bibtex
@article{Jonckers2022,
  author    = {Jonckers, D. and others},
  title     = {Additive Manufacturing of Large Structures Using Free-Flying Satellites},
  journal   = {Frontiers in Space Technologies},
  volume    = {3},
  year      = {2022},
  doi       = {10.3389/frspt.2022.879542},
  url       = {https://doi.org/10.3389/frspt.2022.879542},
  note      = {[Online]. Available: https://www.frontiersin.org/journals/space-technologies/articles/10.3389/frspt.2022.879542/full}
}
```

```bibtex
@conference{VazquezPeralvo2025,
  author    = {Vásquez-Peralvo, J.A. and Talpur, H. and others},
  title     = {Fully Additive Manufactured Ku-Feeder link Antenna for Satellite Communications},
  booktitle = {2025 International Symposium on Antennas and Propagation (ISAP)},
  year      = {2025},
  url       = {https://ieeexplore.ieee.org/document/XXXXXXX},
  note      = {IEEE}
}
```

```bibtex
@conference{Sharma2024,
  author    = {Sharma, A. and others},
  title     = {Satellite Ka-Band Additive Manufactured Antenna},
  booktitle = {IEEE Conference},
  year      = {2024},
  doi       = {10.1109/XXXX.2024.10464704},
  url       = {https://ieeexplore.ieee.org/document/10464704},
  note      = {[Online]. Available: https://ieeexplore.ieee.org/document/10464704}
}
```

**PARTE 3: MAPA DE USO DE REFERENCIAS (POR SECCIÓN)**

```json
{
  "seccion_nro": 1,
  "titulo_seccion": "Introducción",
  "mapa_uso": {
    "Boschetto2023": {
      "razon_seleccion": "Proporciona evidencia cuantitativa de reducción de peso en plataformas satelitales mediante lattice structures fabricadas por PBF-LB/M.",
      "guia_redaccion": "Usar en 1.1 para motivar con datos de ahorro de masa (4-28%) y cumplimiento de frecuencias dinámicas; citar en introducción para contextualizar beneficios en telecom.",
      "subseccion_destino": "1.1"
    },
    "Talpur2025": {
      "razon_seleccion": "Revisión exhaustiva IEEE sobre AM en antenas y RF para SATCOM.",
      "guia_redaccion": "Integrar en 1.2 para destacar flexibilidad de diseño y reducción de costos en componentes RF; mencionar bandas Ku/Ka.",
      "subseccion_destino": "1.2"
    },
    "Dalmarco2026": {
      "razon_seleccion": "Estudio reciente sobre drivers de adopción de AM en sector espacial (reducción de masa y costos).",
      "guia_redaccion": "Citar en 1.3 para resaltar motivación económica y desafíos de calificación.",
      "subseccion_destino": "1.1"
    }
  }
}
```

```json
{
  "seccion_nro": 2,
  "titulo_seccion": "Estado del Arte y Antecedentes",
  "mapa_uso": {
    "Talpur2025": {
      "razon_seleccion": "Estado del arte detallado en AM para antenas SATCOM.",
      "guia_redaccion": "Usar en 2.2 como base principal, comparando técnicas FDM, SLA, DMLS y performance RF.",
      "subseccion_destino": "2.2"
    },
    "Boschetto2023": {
      "razon_seleccion": "Caso específico de rediseño lattice para plataformas.",
      "guia_redaccion": "En 2.3 para ejemplificar optimización estructural.",
      "subseccion_destino": "2.3"
    },
    "Jonckers2022": {
      "razon_seleccion": "Explora manufactura in-situ con satélites free-flying.",
      "guia_redaccion": "Contrastar en 2.1 con enfoques terrestres tradicionales.",
      "subseccion_destino": "2.1"
    }
  }
}
```

```json
{
  "seccion_nro": 3,
  "titulo_seccion": "Metodología de Diseño y Fabricación",
  "mapa_uso": {
    "Boschetto2023": {
      "razon_seleccion": "Metodología detallada de rediseño DfAM con lattice y thickening local.",
      "guia_redaccion": "Base principal para 3.1 y 3.3; describir framework y simulación dinámica.",
      "subseccion_destino": "3.1"
    },
    "VazquezPeralvo2025": {
      "razon_seleccion": "Ejemplo concreto de antena Ku fully additive manufactured.",
      "guia_redaccion": "Apoyar selección de procesos en 3.2.",
      "subseccion_destino": "3.2"
    }
  }
}
```

```json
{
  "seccion_nro": 4,
  "titulo_seccion": "Resultados Experimentales y Análisis",
  "mapa_uso": {
    "Boschetto2023": {
      "razon_seleccion": "Resultados cuantitativos de peso, rigidez y pruebas dinámicas.",
      "guia_redaccion": "Presentar en 4.1 tablas y figuras de ahorro de masa y eigenfrecuencias.",
      "subseccion_destino": "4.1"
    },
    "Talpur2025": {
      "razon_seleccion": "Datos de performance RF de componentes AM.",
      "guia_redaccion": "En 4.2 para métricas de ganancia, bandwidth y eficiencia.",
      "subseccion_destino": "4.2"
    },
    "Sharma2024": {
      "razon_seleccion": "Comparación de métodos de fabricación para antena Ka-Band.",
      "guia_redaccion": "Usar para benchmarking en 4.3 de costos y precisión.",
      "subseccion_destino": "4.3"
    }
  }
}
```

```json
{
  "seccion_nro": 5,
  "titulo_seccion": "Discusión",
  "mapa_uso": {
    "Dalmarco2026": {
      "razon_seleccion": "Análisis de barreras de adopción y calificación en espacio.",
      "guia_redaccion": "En 5.2 para discutir limitaciones reales y costos de cualificación.",
      "subseccion_destino": "5.2"
    },
    "Jonckers2022": {
      "razon_seleccion": "Perspectiva de manufactura orbital para mantenimiento futuro.",
      "guia_redaccion": "Soporte en 5.3 para sostenibilidad y ensamblaje in-orbit.",
      "subseccion_destino": "5.3"
    },
    "Talpur2025": {
      "razon_seleccion": "Limitaciones en materiales y entornos espaciales.",
      "guia_redaccion": "Contrastar beneficios vs desafíos en 5.1.",
      "subseccion_destino": "5.1"
    }
  }
}
```

```json
{
  "seccion_nro": 6,
  "titulo_seccion": "Conclusiones y Trabajos Futuros",
  "mapa_uso": {
    "Boschetto2023": {
      "razon_seleccion": "Conclusiones sobre viabilidad en plataformas.",
      "guia_redaccion": "Sintetizar logros de peso y desempeño en 6.1.",
      "subseccion_destino": "6.1"
    },
    "Dalmarco2026": {
      "razon_seleccion": "Tendencias futuras y predicciones de adopción.",
      "guia_redaccion": "Proponer trabajos en calificación y escalabilidad en 6.3.",
      "subseccion_destino": "6.3"
    }
  }
}
```