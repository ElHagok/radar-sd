# RADAR-SD: Monitoreo Urbano Descentralizado (Protocolo Vanguard)

![Platform](https://img.shields.io/badge/Platform-Android-green.svg)
![License](https://img.shields.io/badge/License-Proprietary-red.svg)
![Status](https://img.shields.io/badge/Status-Active-blue.svg)

**RADAR-SD** es una plataforma descentralizada de monitoreo ciudadano diseñada para la detección y reporte de incidencias en la infraestructura urbana (baches, fallas eléctricas, problemas de agua potable, etc.) mediante una red **P2P (Peer-to-Peer) pura**.

A diferencia de las aplicaciones convencionales basadas en la nube, RADAR-SD **no depende de servidores centrales**. Esto garantiza la operatividad incluso en situaciones de conectividad limitada o nula, protegiendo la soberanía de los datos de los ciudadanos en Santo Domingo y cualquier entorno urbano.

> ⚠️ **Nota de Seguridad:** Este repositorio contiene únicamente la documentación legal (Términos y Condiciones, Política de Privacidad) y archivos estáticos necesarios para la publicación en Google Play Store. El código fuente no está disponible públicamente para prevenir ingeniería inversa y vulnerabilidades en la red P2P.

---

## 🛡️ Arquitectura de Seguridad: Protocolo Vanguard

Para asegurar la integridad de una red sin autoridades centrales, RADAR-SD implementa el **Protocolo Vanguard**, una defensa en profundidad de cuatro capas:

1.  **Ancla de Identidad (Criptografía Asimétrica):**
    *   Cada nodo genera un par de llaves.
    *   Todos los reportes son firmados digitalmente, garantizando que el origen es auténtico y el contenido no ha sido alterado durante la transmisión.

2.  **Filtro de Integridad (Play Integrity API):**
    *   Verificación estricta de hardware y software para asegurar que solo versiones oficiales y dispositivos seguros participen en la red.
    *   Previene la manipulación de límites de tiempo (cooldowns) y el uso de emuladores maliciosos.

3.  **Peaje Antispam (Proof of Work - PoW):**
    *   Cada reporte requiere resolver un acertijo matemático ligero.
    *   Esto impone un costo computacional despreciable para un usuario real, pero prohibitivo para ataques de bots masivos o spam automatizado.

4.  **Juicio Social (Reputación Distribuida):**
    *   Sistema de reputación local gestionado en base de datos.
    *   Los nodos aprenden de interacciones pasadas y pueden vetar automáticamente a emisores de información falsa o maliciosa mediante consenso.

---

## 🧠 Inteligencia Artificial Local

La aplicación integra modelos optimizados (~2MB) que se ejecutan **100% offline** en el dispositivo del usuario:

*   **Visión Artificial:** Clasificación de imágenes en tiempo real para confirmar que el reporte (ej. un bache) es genuino, filtrando falsos positivos como sombras, nubes o asfalto liso.
*   **Análisis de Texto:** Filtrado semántico local de contenido inapropiado, lenguaje abusivo o temas no relacionados antes de que el mensaje sea difundido a la red mesh.

---

## 📡 Conectividad Mesh P2P

Utilizamos la infraestructura de **Google Nearby Connections** para crear una red de malla dinámica y resistente:

*   **Descubrimiento:** Los nodos se encuentran automáticamente mediante Bluetooth de Bajo Consumo (BLE) y Wi-Fi Direct.
*   **Propagación (Gossiping):** Los reportes "saltan" de un dispositivo a otro, expandiendo la cobertura geográfica sin necesidad de internet.
*   **Offline-First:** Diseñada para funcionar completamente sin Internet. La sincronización ocurre cuando cualquier nodo de la red detecta conectividad o se acerca a otros nodos.

---

## 📂 Estructura del Proyecto (Documentación)

Este repositorio sirve como referencia pública para los documentos legales integrados en la aplicación.

| Módulo / Archivo | Descripción |
| :--- | :--- |
| `terms.html` | **Términos y Condiciones:** Reglas de integridad, penalizaciones, uso de recursos y deslinde de responsabilidad. |
| `privacy.html` | **Política de Privacidad:** Manejo de datos, identidad criptográfica, uso de sensores y almacenamiento local. |

---

## ⚖️ Legal y Privacidad

RADAR-SD se rige por la transparencia total y el respeto a la privacidad del usuario.

*   **Sin Rastreadores:** No existen SDKs de terceros ni recolección de datos comerciales.
*   **Identidad Soberana:** Tu identidad en la red está ligada exclusivamente a tu llave criptográfica local, no a tu nombre, email o teléfono.
*   **Acceso Offline Permanente:** Las políticas de privacidad y términos de uso están integradas dentro de la aplicación en formato HTML, accesibles en cualquier momento sin conexión a internet.

### Enlaces Legales (Requeridos por Google Play)

Para cumplir con las normas de Google Play Console, los documentos legales completos están disponibles aquí:

*   📄 [Ver Términos y Condiciones (HTML)](terms.html)
*   🔒 [Ver Política de Privacidad (HTML)](privacy.html)

---

## 📥 Instalación

Puedes descargar la última versión estable directamente desde Google Play Store:

[![Get it on Google Play](https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png)](https://play.google.com/store/apps/details?id=app.askir.radar_sd)

---

*Desarrollado como una iniciativa de infraestructura crítica y monitoreo ciudadano descentralizado.*
