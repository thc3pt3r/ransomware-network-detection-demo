# pcap_descriptions.md – Descripción de muestras de tráfico

Este archivo describe cada uno de los PCAP incluidos en el repositorio y qué señales de ransomware observar.

## 📂 smb_encryption.pcapng

Simula una sesión de cifrado vía protocolo SMB.

🔍 Qué observar:
- Alto volumen de tráfico SMB.
- Nombres de archivos con extensiones como `.locked` o `.encrypted`.
- Escrituras consecutivas y acceso a múltiples shares.
- Posibles ransom notes transferidas como archivos `.txt`.

## 📂 dns_exfiltration.pcapng

Ejemplo de exfiltración de datos utilizando consultas DNS.

🔍 Qué observar:
- Subdominios excesivamente largos.
- Frecuencia alta de queries.
- Patrones repetitivos (tipo DGA).
- Posible resolución a dominios `.onion` o infraestructura sospechosa.

## 📂 clean_traffic.pcapng

Captura de tráfico normal para establecer comparación.

🔍 Qué observar:
- Tráfico SMB legítimo sin anomalías.
- Actividad HTTP básica.
- Consultas DNS a dominios comunes.
- Útil para practicar diferenciación entre tráfico limpio y malicioso.

## 📦 Herramientas recomendadas para análisis

- Wireshark / tshark  
- Zeek  
- Suricata  
- tcpdump
