# Nano 9.3 para antiX 26.1 / Debian Trixie i386

![Nano](https://img.shields.io/badge/Nano-v9.3-blue)
![Platform](https://img.shields.io/badge/Platform-i386-blue)
![antiX](https://img.shields.io/badge/antiX-26.1-green)
![Debian](https://img.shields.io/badge/Debian-Trixie-red)
![License](https://img.shields.io/badge/License-GPLv3-yellow)

Paquete `.deb` del editor **GNU Nano v9.3** compilado para **antiX 26.1 / Debian Trixie (i386, 32 bits)**.

---

## 📋 Tabla de contenidos

- [Características](#-características)
- [Requisitos](#-requisitos)
- [Instalación rápida](#-instalación-rápida)
- [Verificación](#-verificación)
- [Solución de problemas](#-solución-de-problemas)
- [Recompilar desde cero](#-recompilar-desde-cero)
- [Licencia](#-licencia)

---

## ✨ Características

- ✅ Nano **v9.3** (última versión estable al momento de compilar)
- ✅ Compilado para **i386 (32 bits)**
- ✅ Empaquetado como **.deb** instalable con `dpkg`
- ✅ Compatible con **glibc 2.41** (Debian Trixie)

---

## 📦 Requisitos

- **antiX 26.1** (o Debian Trixie i386)
- **Arquitectura i386** (32 bits)
- Dependencias: `libc6`, `libncurses6`

---

## 🚀 Instalación rápida

```bash
wget https://github.com/JOSSEL01/debian-nano-x32/raw/main/packages/nano_9.3-1_i386.deb
sudo dpkg -i nano_9.3-1_i386.deb
sudo apt install -f   # resuelve dependencias si faltan
nano --version
```

Deberías ver: `GNU nano, version 9.3`

---

## ✅ Verificación

```bash
nano --version
# Salida esperada: GNU nano, version 9.3

file $(which nano)
# Salida esperada: ELF 32-bit LSB executable, Intel 80386...
```

---

## 🐛 Solución de problemas

### Error: `version GLIBC_2.42 not found`
Este error ocurre si el paquete fue compilado en un sistema con una versión de glibc más nueva que la de antiX (Debian Trixie usa glibc 2.41). La solución es recompilar dentro de antiX o en un contenedor Debian i386.

---

## 🔨 Recompilar desde cero

Usa el script `build_nano_debian_x32.sh` incluido en este repositorio:

```bash
chmod +x build_nano_debian_x32.sh
./build_nano_debian_x32.sh
```

---

## 📄 Licencia

GNU Nano es software libre bajo la [licencia GPLv3](https://git.savannah.gnu.org/cgit/nano.git/tree/COPYING).

---

## 📞 Contacto

- **Autor:** Jose Andres Mamani Mollericona
- **GitHub:** [@JOSSEL01](https://github.com/JOSSEL01)
- **Repositorio:** [debian-nano-x32](https://github.com/JOSSEL01/debian-nano-x32)
