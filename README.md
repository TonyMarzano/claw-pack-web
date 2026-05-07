# 🐾 Claw Pack — Sitio Web Institucional

> Página web institucional de **Claw Pack**, empresa de transporte de paquetería con sede en San Juan, Argentina.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![AWS EC2](https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square&logo=amazonaws&logoColor=white)

---

## 📋 Descripción

Sitio web institucional de una sola página (landing page) para **Claw Pack**, empresa de transporte y logística de paquetería. Desarrollado con HTML, CSS y JavaScript puro, sin dependencias de frameworks externos. Hosteado en una instancia EC2 de AWS con Nginx como servidor web.

## 🌐 Demo

Accedé al sitio en: `http://98.81.226.244/`

---

## 🗂️ Estructura del proyecto

```
claw-pack-web/
├── index.html                      # Página principal (todo en un solo archivo)
├── clawpack-logo-hd-circle.png     # Logo de la empresa
└── README.md                       # Este archivo
```

---

## ✨ Secciones del sitio

| Sección | Descripción |
|---|---|
| **Hero** | Presentación principal con animaciones y CTA a WhatsApp |
| **Cotizar** | Strip de cotización rápida con enlace directo a WhatsApp |
| **Nosotros** | Historia, valores y métricas de la empresa |
| **Servicios** | Grilla con los 6 servicios principales |
| **Cómo funciona** | Proceso de envío en 4 pasos |
| **Almacenamiento** | Servicios de depósito y logística |
| **Contacto** | Formulario de contacto + datos de la empresa |
| **Sucursales** | Mapas de Google de las 4 sucursales |

---

## 🎨 Stack técnico

- **HTML5 / CSS3 / JavaScript** — Sin frameworks, cero dependencias
- **Google Fonts** — Barlow Condensed + Barlow + Rajdhani
- **Google Maps Embed** — Para las sucursales
- **Nginx** — Servidor web en la instancia EC2
- **AWS EC2** — `t2.micro` con Ubuntu 24.04 LTS

---

## 🚀 Despliegue en EC2

### Requisitos previos
- Instancia EC2 corriendo con Ubuntu 24.04 LTS
- Nginx instalado (`sudo apt install nginx -y`)
- Acceso SSH con tu archivo `.pem`

### Primera vez (clonar el repo)

```bash
# Clonar el repositorio
git clone https://github.com/TonyMarzano/claw-pack-web.git /var/www/html/claw-pack

# Copiar los archivos al directorio de Nginx
sudo cp /var/www/html/claw-pack/index.html /var/www/html/
sudo cp /var/www/html/claw-pack/clawpack-logo-hd-circle.png /var/www/html/

# Ajustar permisos
sudo chmod 644 /var/www/html/index.html
sudo chmod 644 /var/www/html/clawpack-logo-hd-circle.png

# Recargar Nginx
sudo systemctl reload nginx
```

### Actualizaciones posteriores

```bash
deploy.sh
```

> El script `deploy.sh` hace `git pull`, copia los archivos a `/var/www/html/` y recarga Nginx automáticamente.

---

## 🔄 Flujo de trabajo (Git)

```
Editar en PC local  →  git push  →  SSH a EC2  →  deploy.sh  →  ✅ Online
```

```bash
# Desde tu PC local, después de hacer cambios:
git add .
git commit -m "descripción del cambio"
git push

# Desde la instancia EC2:
deploy.sh
```

---

## 📞 Contacto

| Canal | Detalle |
|---|---|
| **WhatsApp** | +54 9 264 630-4664 |
| **Instagram** | @clawpack |
| **Facebook** | /clawpack |
| **Sede** | San Juan, Argentina |

---

## 🗺️ Sucursales

- 📍 San Juan *(Sede Principal)*
- 📍 Buenos Aires
- 📍 Rosario
- 📍 Córdoba

---

## 📄 Licencia

Proyecto privado — © 2026 Claw Pack. Todos los derechos reservados.
