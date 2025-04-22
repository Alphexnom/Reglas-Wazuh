# Reglas-Wazuh

Este repositorio contiene un conjunto de reglas personalizadas para Wazuh, diseñadas específicamente para analizar y detectar eventos generados por Sysmon en sistemas Windows. 
Estas reglas ayudan a mejorar la visibilidad y detección de comportamientos sospechosos o maliciosos.

<div style="margin-top: 40px; text-align: center;">
  <img src="https://github.com/user-attachments/assets/8198d1c9-39b3-4fd0-8347-a5301bb50a7d" alt="Wazuh_blue" style="width: 80px; display: inline-block; margin-right: 90px;"/>
  <img src="https://github.com/user-attachments/assets/2b6d309d-437c-4f28-9ca8-84856fd7d80d" alt="featured" style="width: 190px; display: inline-block;"/>
</div>


## 🎯 Objetivos

Con este enfoque, podrás:

- 🕵️‍♂️ **Detectar amenazas personalizadas**, como procesos no autorizados o cambios críticos.
- 🚨 **Priorizar alertas** según la criticidad (`level`).
- 🧩 **Filtrar reglas por grupos**, utilizando etiquetas como `windows` o `linux`, optimizando el análisis.

---

## 🔧 Instalación de herramientas necesarias

Primero, en el equipo donde se encuentre instalado el **agente Wazuh**, debes descargar los siguientes archivos:

- [Sysmon de Microsoft](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
- [Sysmon-Modular (reglas predefinidas)](https://github.com/olafhartong/sysmon-modular)

---

## 💻 Ejecución del comando

Una vez instalado, ejecutamos el siguiente comando:

![Ejemplo comando](https://user-images.githubusercontent.com/123456789/imagename1.png)

---

## 📊 Resultado esperado

Al finalizar, deberías ver un resultado similar a este:

![Resultado](https://user-images.githubusercontent.com/123456789/imagename2.png)

---

## ✅ Conclusión

Con esto, ya estarían configurados los elementos necesarios en el equipo donde se encuentra el **agente Wazuh**.  
En resumen:

> Se requiere instalar el **agente Wazuh** y **Sysmon**, además de aplicar reglas personalizadas para una detección más precisa y segmentada de eventos.

---

## 📌 Notas adicionales

- Asegúrate de reiniciar el agente tras hacer cambios en la configuración.
- Puedes seguir monitoreando el estado del agente desde el dashboard de Wazuh.
