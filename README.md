# 💰 PCPro - Control de Gastos React

> **Aplicación web moderna para el control inteligente de gastos personales**

![React](https://img.shields.io/badge/React-19.1.1-blue?logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8.3-blue?logo=typescript)
![Vite](https://img.shields.io/badge/Vite-7.1.2-646CFF?logo=vite)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4.1.12-38B2AC?logo=tailwind-css)

---

## 📌 DESCRIPCIÓN DEL PROYECTO

**PCPro Control de Gastos** es una aplicación web moderna y responsive desarrollada en React con TypeScript que permite a los usuarios gestionar sus finanzas personales de manera eficiente e intuitiva. 

### 🎯 **¿Para quién está pensado?**
- 👤 **Personas que buscan control financiero personal**
- 💼 **Profesionales que necesitan organizar sus gastos**
- 🏠 **Familias que quieren optimizar su presupuesto doméstico**
- 📊 **Usuarios que prefieren interfaces modernas y visuales**

---

## ✨ CARACTERÍSTICAS DESTACADAS

- 🎨 **Interfaz moderna y responsive** con TailwindCSS
- 📱 **Diseño mobile-first** adaptable a cualquier dispositivo
- 💾 **Persistencia local** - Los datos se guardan automáticamente
- 🔄 **Gestión de estado avanzada** con useReducer y Context API
- 📊 **Visualización gráfica** con barras de progreso circulares
- 🗂️ **Categorización inteligente** con iconos SVG personalizados
- 📅 **Selector de fechas** integrado para cada gasto
- 🔍 **Filtrado por categorías** para análisis detallado
- ⚡ **Rendimiento optimizado** con Vite y SWC
- 🎭 **Animaciones fluidas** y transiciones suaves

---

## ⚙️ FUNCIONALIDADES

### 💰 **Gestión de Presupuesto**
- Definición de presupuesto inicial
- Cálculo automático de gastos totales
- Visualización del presupuesto restante en tiempo real
- Indicadores visuales de estado financiero

### 📝 **Gestión de Gastos**
- ➕ **Agregar gastos** con nombre, cantidad, categoría y fecha
- ✏️ **Editar gastos existentes** de forma intuitiva
- 🗑️ **Eliminar gastos** con confirmación
- 📋 **Lista completa** de todos los movimientos

### 🏷️ **Sistema de Categorías**
- 💰 Ahorro
- 🍕 Comida
- 🏠 Casa
- 💸 Gastos Varios
- 🎮 Ocio
- 🏥 Salud
- 📺 Suscripciones

### 📊 **Análisis y Reportes**
- Progreso visual con barras circulares
- Filtrado por categorías específicas
- Cálculos automáticos de totales y restantes
- Persistencia de datos en localStorage

---

## 🔧 TECNOLOGÍAS UTILIZADAS

### **Frontend Core**
- ⚛️ **React 19.1.1** - Biblioteca principal de UI
- 🧩 **TypeScript 5.8.3** - Tipado estático y desarrollo robusto
- ⚡ **Vite 7.1.2** - Build tool ultrarrápido
- 🎨 **TailwindCSS 4.1.12** - Framework CSS utility-first

### **Librerías Especializadas**
- 🎛️ **@headlessui/react** - Componentes accesibles sin estilos
- 🎯 **@heroicons/react** - Iconografía moderna
- 📊 **react-circular-progressbar** - Barras de progreso circulares
- 📅 **react-date-picker** - Selector de fechas avanzado
- 📱 **react-swipeable-list** - Listas con gestos táctiles
- 🆔 **uuid** - Generación de identificadores únicos

### **Herramientas de Desarrollo**
- 🔍 **ESLint** - Linting y calidad de código
- 🚀 **SWC** - Compilador ultrarrápido para React
- 📦 **PostCSS & Autoprefixer** - Procesamiento CSS avanzado

---

## 📁 ESTRUCTURA DEL PROYECTO

```
Pcpro Control de gastos react/
├── 📂 public/                    # Recursos estáticos
│   ├── 🖼️ grafico.jpg           # Imagen de demostración
│   └── 🎨 icono_*.svg           # Iconos de categorías
├── 📂 src/
│   ├── 📱 App.tsx               # Componente principal
│   ├── 🧩 components/          # Componentes reutilizables
│   │   ├── BudgetForm.tsx       # Formulario de presupuesto
│   │   ├── BudgetTracker.tsx    # Seguimiento visual
│   │   ├── ExpenseForm.tsx      # Formulario de gastos
│   │   ├── ExpenseList.tsx      # Lista de gastos
│   │   ├── ExpenseModal.tsx     # Modal para gastos
│   │   └── FilterByCategory.tsx # Filtros por categoría
│   ├── 🔄 context/             # Context API
│   │   └── BudgetContext.tsx    # Estado global
│   ├── 📊 data/                # Datos estáticos
│   │   └── categories.ts        # Definición de categorías
│   ├── 🎣 hooks/               # Custom hooks
│   │   └── useBudget.ts         # Hook principal
│   ├── 🔧 reducers/            # Gestión de estado
│   │   └── budget-reducer.ts    # Reducer principal
│   └── 📝 types/               # Definiciones TypeScript
│       └── index.ts             # Tipos principales
├── 📂 docs/                     # Documentación
└── ⚙️ Archivos de configuración # Vite, TS, ESLint, etc.
```

---

## 🚀 INSTRUCCIONES DE USO

### **📋 Prerrequisitos**
- Node.js 18+ instalado
- npm o yarn como gestor de paquetes

### **⬇️ Instalación**

1. **Clonar el repositorio:**
```bash
git clone https://github.com/tu-usuario/pcpro-control-gastos-react.git
cd pcpro-control-gastos-react
```

2. **Navegar al directorio del proyecto:**
```bash
cd "Pcpro Control de gastos react"
```

3. **Instalar dependencias:**
```bash
npm install
# o
yarn install
```

### **🔥 Desarrollo Local**

```bash
# Iniciar servidor de desarrollo
npm run dev
# o
yarn dev
```

La aplicación estará disponible en: `http://localhost:5173`

### **🏗️ Build de Producción**

```bash
# Generar build optimizado
npm run build
# o
yarn build

# Previsualizar build
npm run preview
# o
yarn preview
```

### **🔍 Linting y Calidad**

```bash
# Ejecutar ESLint
npm run lint
# o
yarn lint
```

---

## 🧪 EJEMPLOS DE USO

### **💰 Configuración Inicial**
1. Al abrir la aplicación, define tu presupuesto mensual
2. La interfaz se adaptará mostrando el tracker de gastos

### **📝 Agregar Gastos**
1. Haz clic en el botón "Nuevo Gasto"
2. Completa: nombre, cantidad, categoría y fecha
3. El gasto se agregará automáticamente a tu lista

### **📊 Análisis de Gastos**
1. Usa los filtros por categoría para análisis específicos
2. Observa el progreso visual en las barras circulares
3. Los datos se guardan automáticamente en tu navegador

---

## 📞 Soporte y Contacto

### 🆘 Obtener Ayuda

Si necesitas ayuda con la implementación, personalización o tienes alguna consulta técnica:

📅 **Año:** 2025  
📨 **Autor:** Francisco José Herreros (franHR)  
📧 **Email:** [desarrollo@pcprogramacion.es](mailto:desarrollo@pcprogramacion.es)  
🌐 **Web:** [https://www.pcprogramacion.es](https://www.pcprogramacion.es)  
💼 **LinkedIn:** [Francisco José Herreros](https://linkedin.com/in/francisco-jose-herreros)  

---

## 🖼️ Capturas del Proyecto

*Las capturas de pantalla y demos en vivo estarán disponibles próximamente*

---

## 🛡️ LICENCIA

### **Español**

Copyright (c) 2025 Francisco José Herreros (franHR) / PCProgramación

Todos los derechos reservados.

Este software es propiedad de Francisco José Herreros (franHR), desarrollador de PCProgramación ([https://www.pcprogramacion.es](https://www.pcprogramacion.es)). No está permitido copiar, modificar, distribuir o utilizar este código, ni total ni parcialmente, sin una autorización expresa y por escrito del autor.

El acceso a este repositorio tiene únicamente fines de revisión, auditoría o demostración, y no implica la cesión de ningún derecho de uso o explotación.

Para solicitar una licencia o permiso de uso, contacta con: [desarrollo@pcprogramacion.es](mailto:desarrollo@pcprogramacion.es)

### **English**

Copyright (c) 2025 Francisco José Herreros (franHR) / PCProgramación

All rights reserved.

This software is the property of Francisco José Herreros (franHR), developer of PCProgramación ([https://www.pcprogramacion.es](https://www.pcprogramacion.es)). It is not allowed to copy, modify, distribute or use this code, either totally or partially, without express and written authorization from the author.

Access to this repository has only review, audit or demonstration purposes, and does not imply the transfer of any right of use or exploitation.

To request a license or permission to use, contact: [desarrollo@pcprogramacion.es](mailto:desarrollo@pcprogramacion.es)

---

## 🔝 HASHTAGS RECOMENDADOS PARA LINKEDIN

```
#React #TypeScript #TailwindCSS #Vite #ControlDeGastos #FinanzasPersonales 
#DesarrolloWeb #Frontend #JavaScript #PCProgramacion #WebDevelopment 
#PersonalFinance #BudgetApp #ModernUI #ResponsiveDesign #OpenSource
```

---

<div align="center">

**⭐ Si este proyecto te ha sido útil, no olvides darle una estrella ⭐**

**Desarrollado con ❤️ por [PCProgramación](https://www.pcprogramacion.es)**

</div>