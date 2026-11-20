# Comparador de Seguros Médicos

Página estática (un solo `index.html`) para comparar planes de seguro médico lado a lado y decidir cuál conviene.

**En línea:** https://fnabelardo.github.io/insurance-compare/

## Pestaña 📥 Cargar planes
- **📷 Foto / captura**: lee la imagen con OCR (Tesseract.js) dentro del navegador y rellena prima, deducible, máximo de bolsillo, médico, especialista, genéricos, red y nivel. Hace dos pasadas y marca con ⚠ lo que no coincide.
- **📄 PDF (Summary of Benefits)**: lee el texto del SBC federal con pdf.js y rellena casi todos los campos (consultas prenatales, parto, coaseguro, ejemplos oficiales "Peg/Joe/Mia").
- **✏️ A mano / copiar otro**: plan en blanco o copiando los datos de un plan anterior.
- Siempre muestra una vista previa editable antes de guardar; se puede agregar como plan nuevo o completar uno existente.
- Sin IA y sin servidor: la foto o el PDF nunca salen del navegador. Las librerías se descargan de cdnjs/jsDelivr la primera vez.

## Pestaña 📊 Análisis
- **Normal**: costo anual (prima + copagos) según cuántas visitas esperas y punto de equilibrio entre planes.
- **Embarazada**: calendario prenatal, costo mes a mes por plan y mejor estrategia por períodos (cambiando de plan en cualquier mes o solo el 1 de enero y después del parto). El deducible y el máximo de bolsillo se reinician cada 1 de enero y al cambiar de plan.

Los datos se guardan en el navegador (localStorage) y se pueden exportar/importar como JSON.
