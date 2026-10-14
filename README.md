# Calculadora de poder adquisitivo: instrucciones y cobertura

**Úsala en línea:** https://domingosenpijam.github.io/calculadora-sueldo/

También puedes descargar `index.html` y abrirlo con doble clic en cualquier navegador moderno (Chrome, Firefox, Safari o Edge, en ordenador o móvil). Funciona sin conexión y no envía ningún dato: todo se calcula y se guarda en tu navegador.

## Uso en 5 pasos

1. **Mis datos.** La primera vez verás un *ejemplo ficticio* (marcado en morado). Pulsa «Importar / exportar / borrar → Vaciar tabla» y escribe tus años.
2. Por cada año pon el **bruto anual** (suma de todas las pagas) y, si lo tienes, el **neto anual real** (suma de lo cobrado en nómina). Elige comunidad, edad a 31 de diciembre, hijos, discapacidad y tipo de contrato; pueden cambiar de un año a otro. «Copiar datos personales…» y «Calcular edades…» ahorran trabajo.
   En «Configuración» elige **12 o 14 pagas**: no cambia ningún cálculo anual, solo cómo se reparte el neto en importes mensuales (con 14 pagas, cada paga es el neto anual ÷ 14).
3. Puedes **pegar** columnas desde Excel o Google Sheets (Año, Bruto, Neto) o **importar un CSV** exportado antes.
4. Elige el **modo**: (1) a partir del bruto, con neto estimado (si escribes el neto real de un año, se usa ese), o (2) solo con los netos reales que introduzcas. Elige el **año base** y el **año final** (por defecto, el último año con IPC completo).
5. Mira **Resultados** (tarjetas, explicación, gráficos y tabla completa) y **Desglose fiscal** (bruto, cotizaciones, IRPF y neto por año).

Opcional: activa el **escenario de inflación personal** con tus propias tasas anuales. Va aparte y nunca sustituye al IPC oficial. En «Datos de inflación» puedes corregir cualquier índice del IPC; queda marcado como manual.

«Borrar todos los datos guardados» elimina todo lo almacenado en el navegador.

## Cómo se mide el poder adquisitivo

- IPC general nacional del INE, **media anual** (base 2021), porque los salarios son anuales. No se usa la tasa de diciembre a diciembre.
- Neto real = neto del año × IPC del año base / IPC del año.
- Variación real acumulada = (neto del año / neto base) / (IPC del año / IPC base) − 1.
- Neto necesario = neto base × IPC del año / IPC base. Las tasas nunca se suman: se usan cocientes de índices.
- Si faltan años intermedios, no se inventan: la variación respecto al año anterior disponible se marca con †.
- 2026 tiene un IPC **provisional** (estimación con datos hasta septiembre) y está avisado en pantalla. Por defecto el análisis acaba en 2025.

## Qué calcula realmente el modelo fiscal

**Cotizaciones del trabajador (2015–2026):** contingencias comunes 4,70 %, desempleo 1,55 % (indefinido) o 1,60 % (temporal), formación profesional 0,10 %, MEI (0,10 % en 2023, 0,12 % en 2024, 0,13 % en 2025 y 0,15 % en 2026) y cotización de solidaridad desde 2025, con el tope de la base máxima de cada año.

**IRPF, cuota anual estimada (territorio común, 2015–2026):**
- Gastos deducibles: cotizaciones, 2.000 € de «otros gastos» y el incremento por discapacidad (3.500 o 7.750 €).
- Reducción por rendimientos del trabajo (art. 20) con la regla de cada año, incluida la transitoria de 2018.
- Escala estatal y escala autonómica de cada año, aplicadas de forma progresiva.
- Mínimo personal y familiar (edad, hijos, menores de 3 años, discapacidad), con los importes autonómicos donde la comunidad los cambió.
- Deducción estatal para salarios bajos de 2025 y 2026.
- El bruto necesario para recuperar el poder adquisitivo se obtiene invirtiendo el modelo numéricamente. Solo se muestra si el modelo es aplicable y, cuando hay neto real, si la estimación no se desvía más de un 3 % de él.

**Territorios:** las 15 comunidades de régimen común, de 2015 a 2026 (la tabla de cobertura está en «Fuentes y metodología»). **No se calculan** País Vasco, Navarra, Ceuta y Melilla ni la tributación conjunta: en esos casos introduce el neto real.

## Lo que no contempla (y por qué tu neto real puede ser distinto)

- **Retenciones frente a cuota.** Se estima la cuota anual de la declaración, no las retenciones de la nómina. Lo que te retienen se calcula con otro algoritmo; la diferencia se paga o se devuelve en la renta.
- **Deducciones autonómicas y estatales en cuota:** alquiler, nacimiento, familia numerosa, donativos, vivienda antigua, etc.
- **Otras situaciones:** planes de pensiones, otras rentas (ahorro, alquileres, actividades), ascendientes, descendientes con discapacidad, retribución en especie, atrasos, varios pagadores, cambio de residencia, contratos a tiempo parcial y base mínima de cotización.
- **Simplificaciones:**
  - La cotización de solidaridad se calcula sobre el exceso anual y no mes a mes.
  - En 2018 la base máxima se prorratea (subió en agosto).
  - Galicia 2015, con bases de hasta 17.707,20 €, tenía un tipo único especial que no está modelizado: se pide el neto.
- **Diferencias pequeñas:** las cuotas se calculan sin los redondeos intermedios de Renta WEB y pueden variar en unos euros.

## Fiabilidad de los datos

- **IPC:** índices medios anuales del INE con un decimal, tomados de la reproducción de la tabla anual del INE que publica el CREM de Murcia y contrastados con las tasas medias oficiales del INE y de Funcas. El redondeo a un decimal puede mover las tasas ±0,1 puntos.
- **Reglas fiscales:**
  - Fuentes principales: los Manuales prácticos de Renta de la AEAT, los informes «Tributación Autonómica» del Ministerio de Hacienda, el BOE y los diarios oficiales autonómicos, y las órdenes de cotización.
  - Donde un año solo pudo contrastarse con fuentes secundarias, o se arrastró del año anterior por no haber cambio legal, la tabla de cobertura lo marca con ≈.
  - Pendientes de confirmar:
    - La base máxima de cotización de 2020 (prorrogada de 2019).
    - Madrid y Canarias 2026: se asumen la escala y los mínimos de 2025.
    - Los mínimos de Galicia de 2026: se usan los de 2025.
    - El mínimo por edad mayor de 65 años en Baleares: los manuales de la AEAT no coinciden entre años.
- **Reglas de 2026:** son las conocidas a 14 de octubre de 2026 y pueden cambiar.

## Pruebas realizadas (Chromium)

- **Inflación nula:** el neto real coincide con el nominal y el neto necesario es el neto base.
- **Sueldo constante con inflación del 10 % y del 10 %:** la inflación acumulada es del 21 % (no del 20 %) y la pérdida real del −17,36 %.
- **Neto que crece exactamente igual que la inflación acumulada:** la variación real y la diferencia con el neto necesario son 0.
- **Otros casos:**
  - Años intermedios ausentes, inflación personal compuesta y años anteriores al año base.
  - Caso fiscal comprobado a mano: 2024, Castilla-La Mancha, 30.000 € de bruto. Cotizaciones 1.941 €, IRPF 4.928,70 € y neto 23.130,30 €.
  - Progresividad, inversión bruto↔neto, deducción por salarios bajos, base máxima y cotización de solidaridad.
  - Pegado desde hoja de cálculo, años duplicados, importes a cero, CSV de ida y vuelta, modo neto real y diseño sin desbordamiento horizontal en móvil.

**Es una herramienta orientativa:** no sustituye al cálculo de la Agencia Tributaria ni al asesoramiento fiscal.
