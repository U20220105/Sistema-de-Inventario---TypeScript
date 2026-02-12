# 📦 Sistema de Inventario - TypeScript

Sistema básico de gestión de inventario desarrollado en TypeScript con clase para manejo de productos.

## 📋 Descripción

Este proyecto implementa una clase `Inventario` que permite gestionar productos con sus respectivos atributos como ID, nombre, código, fecha y precio, incluyendo funcionalidad para mostrar información de productos con precios de descuento.

## 🚀 Características

- Clase TypeScript con tipado fuerte
- Gestión de productos de inventario
- Cálculo y visualización de precios con descuento
- Estructura orientada a objetos

## 📦 Prerequisitos

Antes de comenzar, asegúrate de tener instalado:

- **Node.js** (versión 14 o superior)
- **npm** (viene incluido con Node.js)

## 🔧 Instalación

Sigue estos pasos para configurar el proyecto en tu máquina local:

### 1️⃣ Verificar instalación de Node.js y npm

```powershell
node --version
```
Salida esperada: `v24.6.0` (o superior)

```powershell
npm --version
```
Salida esperada: `11.5.1` (o superior)

### 2️⃣ Instalar TypeScript globalmente

```powershell
npm install -g typescript
```

Esto instalará TypeScript de forma global en tu sistema.

### 3️⃣ Verificar instalación de TypeScript

```powershell
tsc --version
```
Salida esperada: `Version 5.9.3` (o superior)

## ▶️ Cómo ejecutar el proyecto

### Compilar el código TypeScript

```powershell
tsc Class.ts
```

Este comando generará un archivo `Class.js` en el mismo directorio.

### Ejecutar el código compilado

```powershell
node Class.js
```

### Salida esperada

```
Producto agregado: Toallas humedad
Código: Psdm32
Fecha: 2026/02/12
Precio base: $2.5
Precios de descuento: $2.45 y $2.4
```

## 🎯 Ejecución rápida (un solo comando)

```powershell
tsc Class.ts && node Class.js
```

## 📁 Estructura del proyecto

```
inventario-typescript/
│
├── Class.ts          # Código fuente TypeScript
├── Class.js          # Código compilado JavaScript (generado)
└── README.md         # Este archivo
```

## 💻 Código de ejemplo

```typescript
class Inventario {
  public id: number;
  public producto: string;
  public codigo: string;
  public fecha: string;
  public precio: number;

  constructor(id: number, producto: string, codigo: string, fecha: string, precio: number) {
    this.id = id;
    this.producto = producto;
    this.codigo = codigo;
    this.fecha = fecha;
    this.precio = precio;
  }

  Agregar(precio2: number, precio3: number): void {
    console.log("Producto agregado: " + this.producto);
    console.log("Código: " + this.codigo);
    console.log("Fecha: " + this.fecha);
    console.log("Precio base: $" + this.precio);
    console.log("Precios de descuento: $" + precio2 + " y $" + precio3);
  }
}

let producto = new Inventario(
  1,
  "Toallas humedad",
  "Psdm32",
  "2026/02/12",
  2.5
);

producto.Agregar(2.45, 2.40);
```

## 🛠️ Tecnologías utilizadas

- **TypeScript** 5.9.3
- **Node.js** 24.6.0
- **npm** 11.5.1

## ⚠️ Solución de problemas

### Error: "tsc no se reconoce"
Si obtienes este error, TypeScript no está instalado correctamente. Ejecuta:
```powershell
npm install -g typescript
```

### Error: "node no se reconoce"
Necesitas instalar Node.js desde [nodejs.org](https://nodejs.org/)

### El código no se actualiza
Recuerda volver a compilar después de hacer cambios:
```powershell
tsc Class.ts
```

## 📝 Notas

- El archivo `.js` es generado automáticamente al compilar
- No es necesario incluir archivos `.js` en el control de versiones (añádelos a `.gitignore`)
- Siempre compila antes de ejecutar después de hacer cambios en el código

## 👤 Autor

**U20220105.**

## 📄 Licencia

Este proyecto es de código abierto y está disponible bajo la Licencia MIT.

---

⭐ Si este proyecto te fue útil, ¡no olvides darle una estrella!
