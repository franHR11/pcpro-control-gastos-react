# 💸 PCPro Control de Gastos

## 📘 Descripción del Proyecto

**PCPro Control de Gastos** es una aplicación web progresiva (PWA) diseñada para la gestión inteligente de finanzas personales. Desarrollada con tecnologías modernas de React y TypeScript, esta solución permite a usuarios individuales y profesionales llevar un control exhaustivo de sus gastos mensuales con una interfaz intuitiva y visualmente atractiva.

### 🎯 Utilidad Real
- **Control financiero personal**: Ideal para freelancers, autónomos y particulares que necesitan llevar un registro detallado de sus gastos
- **Gestión de presupuestos mensuales**: Establece límites de gasto y recibe alertas en tiempo real
- **Análisis de patrones de consumo**: Visualiza tendencias y categorías donde más gastas
- **Toma de decisiones informadas**: Datos claros para optimizar tus finanzas personales

### 👥 Perfil de Usuario Objetivo
- **Freelancers y autónomos** que necesitan controlar gastos de negocio
- **Jóvenes profesionales** que quieren mejorar su educación financiera
- **Familias** que buscan administrar sus finanzas domésticas
- **Estudiantes** aprendiendo sobre gestión financiera personal

## ✨ Características Destacadas

### 🛠️ Funcionalidades Principales
- 📊 **Dashboard interactivo** con gráficos tipo donut y barras
- 💰 **Gestión de presupuestos** dinámica y personalizable
- 📝 **Formulario inteligente** para añadir/editar gastos con validación
- 📱 **Diseño responsive** que funciona en móvil y escritorio
- 🎨 **Interfaz moderna** con Tailwind CSS y animaciones suaves
- 💾 **Persistencia de datos** en localStorage para máxima privacidad

### 🔒 Seguridad y Privacidad
- ⚡ **Sin servidor externo**: Todos los datos se almacenan localmente
- 🔐 **Total privacidad**: Tu información financiera nunca sale de tu dispositivo
- 🔄 **Backup local**: Puedes exportar/importar tus datos fácilmente

### 📊 Análisis Visual
- 🥧 Gráfico de gastos por categoría en tiempo real
- 📈 Indicadores visuales de presupuesto restante
- 🎯 Alertas visuales cuando te acercas al límite de presupuesto
- 📋 Historial completo de gastos con filtros por categoría

## ⚙️ Funcionalidades Detalladas

### Módulos Principales

#### 1. **Sistema de Presupuestos**
- Establecimiento inicial de presupuesto mensual
- Recálculo automático del presupuesto restante
- Visualización clara del estado actual

#### 2. **Gestión de Gastos**
- **Añadir nuevos gastos** con categoría, monto y fecha
- **Editar gastos existentes** con detección de cambios
- **Eliminar gastos** con confirmación visual
- **Búsqueda y filtrado** por categorías

#### 3. **Categorías de Gastos Predefinidas**
- 🍽️ **Comida**: Restaurantes, comida rápida, mercados
- ✈️ **Ocio**: Viajes, cine, entretenimiento
- ⚕️ **Salud**: Medicinas, consultas médicas
- 🏠 **Hogar**: Servicios, mantenimiento
- 💡 **Servicios**: Electricidad, internet, agua
- 🛒 **Varios**: Otros gastos no categorizados

#### 4. **Interfaz de Usuario**
- **Panel principal** con resumen general
- **Formulario modal** para añadir/editar gastos
- **Lista de gastos** con opciones de edición/eliminación
- **Indicadores visuales** de estado del presupuesto

#### 5. **Persistencia y Configuración**
- Almacenamiento automático en localStorage
- Recuperación de datos al reiniciar la aplicación
- Reset opcional del presupuesto y gastos

## 🔧 Tecnologías Utilizadas

### Frontend Stack
- ⚛️ **React 18** - Librería principal de UI
- 🟦 **TypeScript** - Tipado estático y mejor experiencia de desarrollo
- ⚡ **Vite** - Build tool ultrarrápido para desarrollo y producción
- 🎨 **Tailwind CSS** - Framework de CSS utility-first
- 📅 **React Date Picker** - Selector de fechas elegante
- 🆔 **UUID** - Generación de identificadores únicos

### Configuración y Dependencias
```json
{
  "react": "^18.3.1",
  "react-dom": "^18.3.1",
  "react-date-picker": "^11.0.0",
  "uuid": "^10.0.0",
  "tailwindcss": "^3.4.14",
  "typescript": "^5.6.3",
  "vite": "^5.4.10"
}
```

### Herramientas de Desarrollo
- **ESLint** - Análisis estático de código
- **TypeScript** - Compilador y verificación de tipos
- **Vite** - Servidor de desarrollo y build

## 📁 Estructura del Proyecto

```
pcpro-control-gastos-react/
├── public/                    🔗 Archivos públicos y assets
├── src/
│   ├── components/            🧩 Componentes React
│   │   ├── BudgetForm.tsx            # Formulario de presupuesto
│   │   ├── ExpenseForm.tsx           # Formulario de gastos (modal)
│   │   ├── BudgetTracker.tsx         # Tracker principal
│   │   ├── PasoPresupuesto.tsx       # Paso inicial de presupuesto
│   │   └── ErrorMessage.tsx          # Componente de mensajes de error
│   ├── data/                  📊 Datos y utilidades
│   │   └── categories.ts             # Definición de categorías
│   ├── hooks/                 🎣 Custom hooks
│   │   └── useBudget.ts              # Hook principal de gestión de presupuesto
│   ├── reducers/              🔀 Reducers de estado
│   │   └── budget-reducer.ts         # Lógica de estado con reducer pattern
│   ├── types/                 🎯 Definiciones TypeScript
│   │   └── index.ts                  # Tipos de datos de la aplicación
│   ├── App.tsx                🔧 Componente principal
│   └── main.tsx               🚀 Punto de entrada
├── package.json               📦 Configuración de dependencias
├── tsconfig.json              ⚙️ Configuración TypeScript
├── tailwind.config.js         🎨 Configuración Tailwind CSS
├── vite.config.ts             ⚡ Configuración Vite
└── README.md                  📘 Este archivo
```

## 🚀 Instrucciones de Uso

### Requisitos Previos
- **Node.js** 16.0 o superior
- **npm** o **yarn** como gestor de paquetes

### Instalación Local

1. **Clonar el repositorio**:
```bash
git clone [URL_DEL_REPOSITORIO]
cd pcpro-control-gastos-react
```

2. **Instalar dependencias**:
```bash
npm install
```

3. **Configurar variables de entorno** (opcional):
```bash
# Crear archivo .env.local
VITE_APP_VERSION=1.0.0
VITE_APP_TITLE="PCPro Control de Gastos"
```

4. **Iniciar servidor de desarrollo**:
```bash
npm run dev
```

### Build para Producción

```bash
# Construir para producción
npm run build

# Previsualizar build
npm run preview
```

### Despliegue en Producción

#### Opción 1: Netlify/Vercel (Recomendado)
1. Conectar tu repositorio Git con Netlify o Vercel
2. Configurar:
   - **Build Command**: `npm run build`
   - **Publish Directory**: `dist`

#### Opción 2: GitHub Pages
```bash
npm run build
# Subir contenido de la carpeta 'dist' a gh-pages
```

## 🧪 Ejemplos de Uso

### Caso 1: Añadir primer gasto
1. Abrir la aplicación
2. Establecer presupuesto mensual (ej: €1,500)
3. Click en "Nuevo Gasto"
4. Rellenar:
   - Nombre: "Cena restaurante"
   - Cantidad: 45.50
   - Categoría: Comida
   - Fecha: [fecha actual]
5. Ver el resumen actualizado automáticamente

### Caso 2: Editar gasto existente
1. Buscar el gasto en la lista
2. Click en "Editar"
3. Modificar cualquier campo
4. Guardar cambios
5. Ver actualización del presupuesto

### Caso 3: Filtrar por categoría
1. Ver la lista de gastos en la parte inferior
2. Usar filtros por categoría disponibles
3. Ver solo gastos de esa categoría específica

## 🆘 Soporte y Contacto

### 📅 Año
2025

### 📨 Autor
**Francisco José Herreros (franHR)**
Desarrollador Full Stack & Consultor de Software

### 📧 Contacto
- **Email**: desarrollo@pcprogramacion.es
- **Web**: https://www.pcprogramacion.es
- **LinkedIn**: Francisco José Herreros

### 🌐 Redes Sociales
- **Portfolio**: https://www.pcprogramacion.es
- **GitHub**: [Tu perfil de GitHub]
- **LinkedIn**: [LinkedIn/Directorio]

## 📈 Estadísticas del Proyecto

- **Líneas de código**: ~1,200 línes TypeScript
- **Componentes React**: 6 componentes principales
- **Tests unitarios**: Pendiente de implementación
- **Dependencias**: 6 principales + 8 de desarrollo
- **Bundle size**: ~200KB gzip (optimizado con Vite)

## 🖼️ Capturas de Pantalla

### Dashboard Principal
[Captura del dashboard con presupuesto actual, gastos y gráficos]

### Formulario de Gastos
[Captura del modal para añadir/editar gastos con todos los campos]

### Vista Responsive
[Captura en móvil mostrando perfecta adaptación]

## 🛡️ Licencia

### Español
Copyright (c) 2025 Francisco José Herreros (franHR) / PCProgramación

**Todos los derechos reservados.**

Este software es propiedad de Francisco José Herreros (franHR), desarrollador de PCProgramación. No está permitido copiar, modificar, distribuir o utilizar este código, ni total ni parcialmente, sin una autorización expresa y por escrito del autor.

El acceso a este repositorio tiene únicamente fines de revisión, auditoría o demostración, y no implica la cesión de ningún derecho de uso o explotación.

Para solicitar una licencia o permiso de uso, contacta con: desarrollo@pcprogramacion.es

### English
Copyright (c) 2025 Francisco José Herreros (franHR) / PCProgramación

**All rights reserved.**

This software is the property of Francisco José Herreros (franHR), developer of PCProgramación. It is not allowed to copy, modify, distribute or use this code, either totally or partially, without express and written authorization from the author.

Access to this repository has only review, audit or demonstration purposes, and does not imply the transfer of any right of use or exploitation.

To request a license or permission to use, contact: desarrollo@pcprogramacion.es

## 🔝 Hashtags Recomendados para LinkedIn

### Para compartir este proyecto:
- `#React` `#TypeScript` `#PersonalFinance` `#WebDevelopment`
- `#TailwindCSS` `#PWA` `#OpenSource` `#FullStack`
- `#BudgetManager` `#ExpenseTracker` `#NodeJS`
- `#Vite` `#ModernWeb` `#DeveloperPortfolio`
- `#ReactHooks` `#StateManagement` `#ResponsiveDesign`

### Frases para posts de LinkedIn:
"🎯 Nueva herramienta para control financiero personal: PCPro Control de Gastos. Desarrollada con React + TypeScript + Vite 🔥"

"📊 ¿Necesitas controlar tus gastos mensuales? Esta app PWA te ayuda a mantener tu presupuesto en orden #PersonalFinance"

"⚡ De 0 a productivo: aplicación de control de gastos en producción con tecnologías modernas de React"

---

<p align="center">
  <strong>💼 ¿Necesitas esta aplicación para tu negocio o quieres contratar mis servicios?</strong><br>
  <a href="mailto:desarrollo@pcprogramacion.es">📧 desarrollo@pcprogramacion.es</a> | 
  <a href="https://www.pcprogramacion.es">🌐 www.pcprogramacion.es</a>
</p>