# Investment Copilot

Investment Copilot es un marco de análisis de inversiones para estructurar la investigación de acciones y ETFs, valorar escenarios y entender el papel de cada posición en una cartera.

Su propósito es mejorar el proceso de razonamiento. No sustituye el juicio del usuario ni presenta sus conclusiones como órdenes de compra o venta.

## Principios

- Entender el activo antes de valorar su precio.
- Separar datos reportados, cálculos, estimaciones y supuestos.
- Valorar mediante rangos y escenarios, no con una cifra de precisión falsa.
- Explicar qué expectativas parece reflejar el mercado.
- Buscar evidencia que contradiga la tesis.
- Evaluar el encaje en cartera cuando el usuario aporte datos suficientes.
- Fechar y citar la información material.

## Arquitectura

`CORE → Stock Analyzer o ETF Analyzer → Valuation Engine → Portfolio Analyzer (si hay datos) → Decision Framework`

El protocolo de fuentes y seguimiento se aplica a todos los módulos. El Decision Framework puede operar sin datos de cartera, pero debe señalar que el encaje individual no fue evaluado.

## Módulos

- [CORE](docs/core.md): misión, filosofía y reglas generales.
- [Stock Analyzer](docs/stock-analyzer.md): análisis fundamental de acciones.
- [ETF Analyzer](docs/etf-analyzer.md): análisis de mandato, composición, costos y riesgo de ETFs.
- [Valuation Engine](docs/valuation-engine.md): métodos, escenarios y sensibilidad.
- [Portfolio Analyzer](docs/portfolio-analyzer.md): exposiciones, concentración y solapamientos.
- [Decision Framework](docs/decision-framework.md): síntesis condicional de la evidencia.
- [Data & Monitoring Protocol](docs/data-monitoring.md): fuentes, fechas, verificación y seguimiento.

## Estado

Especificación de diseño v1.0. Esta documentación no implementa integraciones de datos, cálculos automáticos ni ejecución de operaciones.

## Uso

Indica el activo y la pregunta concreta: entender el negocio, revisar la valoración, comparar ETFs o evaluar el encaje en cartera. Si el análisis requiere datos de cartera, proporciona posiciones y pesos o valores de mercado.

