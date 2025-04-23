# 🛠️ CREAR REGLA PERSONALIZADA EN WAZUH

En esta guía aprenderás a crear reglas personalizadas en **Wazuh** para monitorear eventos específicos, como actividades sospechosas en sistemas Windows detectadas por **Sysmon**.  
Además, veremos cómo asignar estas reglas a **grupos de agentes**, permitiendo una gestión segmentada y eficiente según el tipo de dispositivo (por ejemplo: servidores, estaciones de trabajo).



##  Objetivos

Con este enfoque, podrás:

- **Detectar amenazas personalizadas**, como procesos no autorizados o cambios críticos.
- **Priorizar alertas** según la criticidad (`level`).
- **Filtrar reglas por grupos**, utilizando etiquetas como `windows` o `linux`, optimizando el análisis.



##  El primer paso es instalar Sysmon en el equipo donde está el agente Wazuh

En el equipo donde se encuentre instalado el **agente Wazuh**, debes descargar los siguientes archivos:

- [Sysmon de Microsoft](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
- [Sysmon-Modular (reglas predefinidas)](https://github.com/olafhartong/sysmon-modular)



##  Ejecución del comando

Una vez instalado, ejecutamos el siguiente comando:

![Image](https://github.com/user-attachments/assets/29d34f98-288e-497d-94d0-583914ac0a35)



##  Resultado esperado tras instalar Sysmon

Al finalizar, deberías ver un resultado similar a este:

![Image](https://github.com/user-attachments/assets/922671ff-656b-426d-8e3a-18938fc1d8b8)






## 📌 Configuración de Reglas Personalizadas en Wazuh

En Wazuh configuraremos dos puntos importantes: **una nueva regla personalizada** y **una regla para los grupos**.

### Paso 1: Agregar una nueva regla en el grupo

Primero, agrega la nueva regla en el grupo correspondiente (las reglas están disponibles en el repositorio en la siguiente ruta, solo tienes que copiar y pegarlas):

![Imagen de la ruta en el repositorio](https://github.com/user-attachments/assets/aa31a0de-f486-423b-a5a0-652ba1e3d3fd)

1. Copia el archivo de la regla desde el repositorio.

2. Pega el archivo copiado en las siguientes rutas de tu equipo:

   - **1ª ruta**:  
     ![Imagen de la primera ruta](https://github.com/user-attachments/assets/b748570e-ce3b-40fe-8bc1-31b20c71e951)

   - **2ª ruta**:  
     ![Imagen de la segunda ruta](https://github.com/user-attachments/assets/4a7bcc7e-3444-47ac-b0bd-95bf84c4a369)

   - **3ª ruta**:  
     ![Imagen de la tercera ruta](https://github.com/user-attachments/assets/9aaf5fed-5568-41d0-b03e-c942d034bad9)

Guardas los cambios y con esto, habrás asignado la regla al grupo que hayas creado, en mi caso, **Windows**.

---

### Paso 2: Agregar la regla de Sysmon en Wazuh

Ahora, configuraremos una nueva regla de **Sysmon** en la siguiente ruta de Wazuh:

1. **1ª ruta**:  
   ![Imagen de la primera ruta](https://github.com/user-attachments/assets/5c00ff8d-c772-45d2-a234-2812bee18966)

2. **2ª ruta**:  
   ![Imagen de la segunda ruta](https://github.com/user-attachments/assets/fff191b9-4a78-4d34-ba7b-1089959540ba)

3. **3ª ruta**:  
   ![Imagen de la tercera ruta](https://github.com/user-attachments/assets/9d0b40a4-1b7a-4699-b2d2-e1b6e486ba15)

4. Agrega la siguiente regla que está en mi repositorio en la siguiente ruta, es solo copiarla:

   - **4ª ruta**:  
     ![Imagen de la cuarta ruta](https://github.com/user-attachments/assets/058b778f-dbc9-4369-9979-addc05275e7d)

5. Una vez copiada la regla del repositorio, la pegaremos en la configuración de Wazuh.
   - **5ª ruta**:  
     ![Imagen de la quinta ruta](https://github.com/user-attachments/assets/ddd7820d-3cff-4fc6-b0ad-5484b97ea4b3)

Con esto, habrás implementado la nueva regla **Sysmon** para que Wazuh pueda detectar eventos relacionados.

---

## 📌 IMPORTANTE

- Asegúrate de reiniciar el agente tras hacer cambios en la configuración.
 
   ![Imagen de reinicio del agente](https://github.com/user-attachments/assets/d61510fa-e08c-4740-bb69-5648a6ad36c4)
