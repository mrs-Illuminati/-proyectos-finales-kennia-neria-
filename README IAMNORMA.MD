KENNIA JANETTE NERIA BARAJAS

SEBASTIAN ALAN FERNANDEZ OROZCO



PROYECTO WomenCiso-MenCiso
IAM NORMA 


Este documento presenta un framework de cuatro capas, construido sobre herramientas de Google Cloud, para mitigar las vulnerabilidades de API más relevantes para una empresa fintech digital mexicana hipotética. Cada capa se describe bajo el mismo formato: el problema técnico que atiende, la solución específica de Google que lo mitiga, y el impacto económico estimado, anclado a benchmarks públicos verificables (no cifras inventadas).

El Framework de IA Security para APIs es una plataforma que combina cuatro capas de defensa ya probadas de Google Cloud (Fraud Defense, Cloud Armor, Apigee Advanced API Security y Model Armor) con un motor propio de orquestación que traduce los hallazgos técnicos al lenguaje regulatorio mexicano y sugiere remediación automática — una combinación innovadora porque ningún competidor global ni local ofrece hoy remediación automática nativa sobre infraestructura de Google Cloud con ese enfoque regulatorio; viable porque reduce el riesgo técnico al construirse sobre infraestructura ya probada a escala en vez de detección desde cero; y con impacto en tres dimensiones: económico (reducción de pérdida esperada por incidente, medible vía metodología ALE/FAIR), regulatorio (reducción del tiempo y esfuerzo de reporte a CNBV/Condusef) y de confianza de mercado (acelera el due diligence de seguridad que exigen inversionistas y socios enterprise de la fintech cliente).
Arquitectura de 4 capas construida sobre productos nativos de Google Cloud:

●	Capa 1 — Google Cloud Fraud Defense (reCAPTCHA Enterprise): detección de bots, fraude de pagos y toma de cuentas.
Costo promedio por registro de PII comprometido = $160 USD (IBM 2025). Fórmula aplicable: costo estimado = (número de cuentas comprometidas en un escenario de ATO no mitigado) × $160 USD.
Techo de referencia sectorial: $5.56M USD (promedio de brecha en servicios financieros, IBM 2025, global).
Cloud Armor filtra y absorbe tráfico de ataque en el borde de la red de Google antes de que llegue a los clústeres o endpoints backend, bloqueando payloads maliciosos como XSS y registrando el intento.

●	Capa 2 — Cloud Armor: WAF perimetral contra inyección, XSS y DDoS. 
Costo promedio de recuperación de un incidente de ransomware sin pago de rescate = $1.53M USD (IBM 2025). Se usa como referencia porque una interrupción de disponibilidad no contenida en el perímetro es frecuentemente la puerta de entrada a un incidente de ransomware.

●	Capa 3 — Apigee Advanced API Security: detección de BOLA/BFLA vía ML, validación de OAuth2/OIDC/JWT, descubrimiento de APIs no documentadas.
Apigee Advanced API Security evalúa continuamente proxies de API y tráfico, identificando configuraciones incorrectas que podrían derivar en BFLA, con recomendaciones accionables para poner controles de acceso faltantes.
La detección de abuso usa modelos de machine learning para detectar y bloquear solicitudes maliciosas. Valida que OAuth 2.0, OpenID Connect y JWT estén configurados correctamente.costo por registro de PII financiera comprometido = $160 USD/registro; costo por registro de propiedad intelectual comprometido (p. ej. lógica de scoring crediticio expuesta vía BOLA) = $178 USD/registro, la categoría más cara medida por IBM.
Techo de referencia sectorial: $5.56M USD (servicios financieros, IBM 2025).

●	Capa 4 — Model Armor + AI Protection: protección contra prompt injection y fuga de datos si la fintech expone agentes de IA (chatbots, KYC automatizado) vía API.
Model Armor protege contra inyección de prompts, jailbreak, pérdida de datos, URLs maliciosas y contenido ofensivo. AI Protection en Security Command Center aporta inventario y detección de amenazas para cargas de trabajo agénticas.
Nota de madurez: el soporte de AI Protection para cargas agénticas vía servidores MCP está en Preview, no en disponibilidad general (GA), al momento de este documento.
La capa propietaria que convierte esto de "arquitectura de referencia" en producto invertible: un motor que (a) traduce los hallazgos técnicos de las 4 capas al lenguaje de reporte regulatorio mexicano, y (b) genera automáticamente la remediación sugerida (no solo la alerta) para el hallazgo de mayor frecuencia — BOLA/BFLA en Apigee.

 
