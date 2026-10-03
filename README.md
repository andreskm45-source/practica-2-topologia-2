## Infraestructura 2: Entorno Multi-Vendor (Cisco a FortiGate)

https://itlaedudo-my.sharepoint.com/:v:/g/personal/20250784_itla_edu_do/IQDjGbFi9LpPSatsyKn5Li95AeW_0C7iGSen4a5urm5GxcY?e=IcJRqa&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

Esta topología simula un entorno corporativo heterogéneo, integrando un router Cisco c7200 en la sede de usuarios y un FortiGate en la sede del servidor[cite: 25]. Requiere parametrización criptográfica manual para asegurar la compatibilidad de las Fases 1 y 2 de IPsec.

<img width="749" height="622" alt="image" src="https://github.com/user-attachments/assets/385444dd-e92f-4b45-948c-0a8275efe5f6" />
<img width="975" height="359" alt="image" src="https://github.com/user-attachments/assets/ceb95d6c-5a82-48fc-868f-a9fff5854213" />


### Parámetros de Criptografía (Custom IPsec)
*   **Algoritmo de Encriptación:** DES
*   **Algoritmo de Hashing:** MD5
*   **Grupo Diffie-Hellman:** Group 2
*   **Autenticación:** Pre-Shared Key (PSK)
*   **PFS & Replay Detection:** Deshabilitados (Requisito de compatibilidad IOS/FortiOS).

### Validaciones Realizadas
*   ✅ Configuración por CLI en Cisco (NAT overload con exclusión de ACL para la VPN).
*   ✅ Emparejamiento exitoso (ISAKMP SA / IPsec SA) entre tecnologías de distintos fabricantes.
*   ✅ Demostración de interrupción de servicio: Al deshabilitar administrativamente la interfaz del túnel, la comunicación con el servidor web se bloquea instantáneamente.# practica-2-topologia-2
