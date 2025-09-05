# 💰 PCPro - Control de Gastos React

> **Aplicación web moderna para gestión inteligente de presupuestos personales**

[![React](https://img.shields.io/badge/React-19.1.1-61DAFB?style=for-the-badge&logo=react)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8.3-3178C6?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-7.1.2-646CFF?style=for-the-badge&logo=vite)](https://vitejs.dev/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-4.1.12-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)

---

## 📌 DESCRIPCIÓN DEL PROYECTO

**PCPro Control de Gastos** es una aplicación web moderna y responsive desarrollada con React y TypeScript que permite a los usuarios gestionar sus finanzas personales de manera intuitiva y eficiente.

### 🎯 **¿Para quién está pensado?**
- 👤 **Personas individuales** que buscan controlar sus gastos mensuales
- 👨‍👩‍👧‍👦 **Familias** que necesitan organizar su presupuesto doméstico
- 💼 **Freelancers y emprendedores** que requieren seguimiento de gastos profesionales
- 🎓 **Estudiantes** que desean aprender a administrar su dinero

### 💡 **Utilidad Real**
Permite establecer un presupuesto inicial y realizar un seguimiento detallado de todos los gastos, categorizándolos y visualizando el progreso mediante gráficos circulares interactivos. Los datos se mantienen persistentes en el navegador para una experiencia continua.

---

## ✨ CARACTERÍSTICAS DESTACADAS

### 🛠️ **Gestión de Presupuesto**
- 💰 Definición de presupuesto inicial personalizable
- 📊 Visualización del progreso con barras circulares animadas
- 🔄 Cálculo automático de gastos totales y presupuesto restante
- ⚠️ Alertas visuales cuando se alcanza el 100% del presupuesto

### 📦 **Control de Gastos**
- ➕ Registro rápido de nuevos gastos
- ✏️ Edición y eliminación de gastos existentes
- 📅 Selección de fechas con calendario interactivo
- 🏷️ Categorización automática con iconos personalizados

### 🎨 **Experiencia de Usuario**
- 📱 Diseño responsive para móviles, tablets y desktop
- 🎭 Interfaz moderna con animaciones suaves
- 🔍 Sistema de filtrado por categorías
- 💾 Persistencia automática de datos en localStorage

### 🔒 **Seguridad y Rendimiento**
- ⚡ Carga ultrarrápida con Vite
- 🧩 Tipado estático con TypeScript
- 🛡️ Validación de formularios en tiempo real
- 📊 Optimización de re-renders con React hooks

---

## ⚙️ FUNCIONALIDADES

### 🏠 **Módulo Principal (App.tsx)**
- Control de estado global con Context API
- Renderizado condicional según presupuesto definido
- Persistencia automática en localStorage
- Gestión de modales y componentes dinámicos

### 💳 **Gestión de Presupuesto**
- **BudgetForm**: Formulario para establecer presupuesto inicial
- **BudgetTracker**: Visualización del progreso con gráfico circular
- **AmountDisplay**: Componente reutilizable para mostrar cantidades

### 📝 **Gestión de Gastos**
- **ExpenseForm**: Formulario completo para crear/editar gastos
- **ExpenseList**: Lista interactiva de todos los gastos
- **ExpenseDetail**: Vista detallada de cada gasto individual
- **ExpenseModal**: Modal responsive para gestión de gastos

### 🎛️ **Componentes de Control**
- **FilterByCategory**: Sistema de filtrado por categorías
- **ErrorMessage**: Manejo centralizado de errores
- Sistema de validación en tiempo real

### 📊 **Categorías Disponibles**
- 💰 Ahorro
- 🍕 Comida
- 🏠 Casa
- 💸 Gastos Varios
- 🎮 Ocio
- 🏥 Salud
- 📺 Suscripciones

---

## 🔧 TECNOLOGÍAS UTILIZADAS

### **🚀 Frontend Core**
- ⚛️ **React 19.1.1** - Biblioteca principal de UI con las últimas características
- 🧩 **TypeScript 5.8.3** - Tipado estático para desarrollo robusto
- ⚡ **Vite 7.1.2** - Build tool de nueva generación ultrarrápido
- 🎨 **TailwindCSS 4.1.12** - Framework CSS utility-first moderno

### **📚 Librerías Especializadas**
- 🎛️ **@headlessui/react 2.2.7** - Componentes accesibles sin estilos predefinidos
- 🎯 **@heroicons/react 2.2.0** - Iconografía moderna y optimizada
- 📊 **react-circular-progressbar 2.2.0** - Gráficos circulares interactivos
- 📅 **react-date-picker 12.0.1** - Selector de fechas avanzado
- 📱 **react-swipeable-list 1.10.0** - Listas con gestos táctiles
- 🆔 **uuid 11.1.0** - Generación de identificadores únicos

### **🛠️ Herramientas de Desarrollo**
- 📋 **ESLint 9.33.0** - Linting y análisis de código
- 🎨 **Prettier** (integrado) - Formateo automático de código
- 🔧 **PostCSS 8.5.6** - Procesamiento avanzado de CSS
- ⚙️ **Autoprefixer 10.4.21** - Compatibilidad automática de CSS

---

## 📁 ESTRUCTURA DEL PROYECTO

```
pcpro-control-gastos-react/
├── 📂 Pcpro Control de gastos react/     # Aplicación principal
│   ├── 📂 src/
│   │   ├── 📄 App.tsx                   # Componente principal
│   │   ├── 📄 main.tsx                  # Punto de entrada
│   │   ├── 📂 components/               # Componentes reutilizables
│   │   │   ├── 💰 BudgetForm.tsx        # Formulario de presupuesto
│   │   │   ├── 📊 BudgetTracker.tsx     # Seguimiento visual
│   │   │   ├── 📝 ExpenseForm.tsx       # Formulario de gastos
│   │   │   ├── 📋 ExpenseList.tsx       # Lista de gastos
│   │   │   ├── 🔍 FilterByCategory.tsx  # Filtros por categoría
│   │   │   └── 🎭 ExpenseModal.tsx      # Modal de gestión
│   │   ├── 📂 context/                  # Context API para estado global
│   │   │   └── 🔄 BudgetContext.tsx     # Contexto principal
│   │   ├── 📂 reducers/                 # Lógica de estado
│   │   │   └── ⚙️ budget-reducer.ts     # Reducer principal
│   │   ├── 📂 hooks/                    # Custom hooks
│   │   │   └── 🎣 useBudget.ts          # Hook personalizado
│   │   ├── 📂 types/                    # Definiciones TypeScript
│   │   │   └── 📋 index.ts              # Tipos principales
│   │   └── 📂 data/                     # Datos estáticos
│   │       └── 🏷️ categories.ts         # Categorías disponibles
│   ├── 📂 public/                       # Recursos estáticos
│   │   ├── 🖼️ grafico.jpg              # Imagen de demostración
│   │   └── 🎨 icono_*.svg              # Iconos de categorías
│   ├── ⚙️ vite.config.ts               # Configuración de Vite
│   ├── 📋 package.json                 # Dependencias del proyecto
│   └── 🎨 tailwind.config.js          # Configuración de Tailwind
├── 📂 docs/                            # Documentación del proyecto
│   ├── 📖 README.md                   # Documentación principal
│   ├── 📝 MEMORIAS.md                 # Registro de cambios
│   └── ✅ CHECKLIST_RUTAS.md          # Lista de tareas
└── 📚 react-libraries-guide.md        # Guía de librerías React
```

---

## 🚀 INSTRUCCIONES DE USO

### **📦 Instalación de Dependencias**

```bash
# Navegar al directorio del proyecto
cd "Pcpro Control de gastos react"

# Instalar dependencias con npm
npm install

# O con yarn
yarn install

# O con pnpm (recomendado para mejor rendimiento)
pnpm install
```

### **⚙️ Configuración del Entorno**

```bash
# No requiere variables de entorno adicionales
# La aplicación usa localStorage para persistencia
```

### **🔥 Levantar el Entorno de Desarrollo**

```bash
# Iniciar servidor de desarrollo
npm run dev

# La aplicación estará disponible en:
# http://localhost:5173
```

### **🏗️ Build para Producción**

```bash
# Generar build optimizado
npm run build

# Previsualizar build de producción
npm run preview

# Los archivos se generarán en la carpeta 'dist/'
```

### **🧹 Linting y Formateo**

```bash
# Ejecutar linting
npm run lint

# Corregir errores automáticamente
npm run lint -- --fix
```

---

## 🧪 EJEMPLOS DE USO

### **💰 Establecer Presupuesto Inicial**
```typescript
// El usuario ingresa su presupuesto mensual
const budget = 1500; // €1,500 mensuales

// El sistema calcula automáticamente:
// - Gastos totales: €0
// - Presupuesto restante: €1,500
// - Porcentaje gastado: 0%
```

### **📝 Registrar un Nuevo Gasto**
```typescript
// Ejemplo de gasto registrado
const newExpense = {
  expenseName: "Compra semanal supermercado",
  amount: 85.50,
  category: "Comida",
  date: new Date("2025-01-15")
};

// El sistema actualiza automáticamente:
// - Total gastado: €85.50
// - Presupuesto restante: €1,414.50
// - Porcentaje: 5.7%
```

### **🔍 Filtrar Gastos por Categoría**
```typescript
// Filtrar solo gastos de "Comida"
const foodExpenses = expenses.filter(expense => 
  expense.category === "Comida"
);

// Calcular total por categoría
const totalFood = foodExpenses.reduce((sum, expense) => 
  sum + expense.amount, 0
);
```

---

## 🖼️ Capturas del Proyecto

### 🏠 **Pantalla Principal**
- Formulario de presupuesto inicial limpio y moderno
- Diseño responsive que se adapta a cualquier dispositivo

### 📊 **Dashboard de Control**
- Gráfico circular animado mostrando el progreso del gasto
- Tarjetas informativas con presupuesto, gastado y disponible
- Botón de reinicio para comenzar un nuevo período

### 📝 **Gestión de Gastos**
- Modal elegante para agregar/editar gastos
- Selector de categorías con iconos personalizados
- Calendario interactivo para selección de fechas
- Lista de gastos con opciones de edición y eliminación

### 🔍 **Sistema de Filtros**
- Filtrado dinámico por categorías
- Actualización en tiempo real de la lista
- Indicadores visuales del filtro activo

---

## 📞 Soporte y Contacto

### 🆘 **Obtener Ayuda**

Si necesitas ayuda con la instalación, configuración o uso de la aplicación:

1. 📧 **Email directo**: [desarrollo@pcprogramacion.es](mailto:desarrollo@pcprogramacion.es)
2. 🌐 **Sitio web oficial**: [https://www.pcprogramacion.es](https://www.pcprogramacion.es) <mcreference link="https://www.pcprogramacion.es" index="0">0</mcreference>
3. 💼 **LinkedIn**: [Francisco José Herreros](https://linkedin.com/in/francisco-jose-herreros)
4. 📱 **Consulta gratuita**: Disponible a través del sitio web

### 👨‍💻 **Sobre el Desarrollador**

**Francisco José Herreros (franHR)** - CEO de PCProgramación <mcreference link="https://www.pcprogramacion.es" index="0">0</mcreference>

> *"Como director ejecutivo de PCpro, he liderado con determinación, buscando siempre esclarecer los requisitos y optimizar cada minuto para asegurar los mejores resultados. En PCpro, me he asegurado de que lo que parecía complicado se convierta en una realidad alcanzable para nuestros clientes."* <mcreference link="https://www.pcprogramacion.es" index="0">0</mcreference>

### 🏢 **Servicios Disponibles**
- 💻 **Desarrollo de Software Personalizado**
- ☁️ **Soluciones en la Nube**
- 🤖 **Integración de IA y Machine Learning**
- 📊 **Consultoría Empresarial**
- 🎓 **Formación y Capacitación Técnica**

---

## 🛡️ LICENCIA

### **Español**

**Copyright (c) 2025 Francisco José Herreros (franHR) / PCProgramación**

**Todos los derechos reservados.**

Este software es propiedad de Francisco José Herreros (franHR), desarrollador de PCProgramación ([https://www.pcprogramacion.es](https://www.pcprogramacion.es)). No está permitido copiar, modificar, distribuir o utilizar este código, ni total ni parcialmente, sin una autorización expresa y por escrito del autor.

El acceso a este repositorio tiene únicamente fines de revisión, auditoría o demostración, y no implica la cesión de ningún derecho de uso o explotación.

**Para solicitar una licencia o permiso de uso, contacta con**: [desarrollo@pcprogramacion.es](mailto:desarrollo@pcprogramacion.es)

### **English**

**Copyright (c) 2025 Francisco José Herreros (franHR) / PCProgramación**

**All rights reserved.**

This software is the property of Francisco José Herreros (franHR), developer of PCProgramación ([https://www.pcprogramacion.es](https://www.pcprogramacion.es)). It is not allowed to copy, modify, distribute or use this code, either totally or partially, without express and written authorization from the author.

Access to this repository has only review, audit or demonstration purposes, and does not imply the transfer of any right of use or exploitation.

**To request a license or permission to use, contact**: [desarrollo@pcprogramacion.es](mailto:desarrollo@pcprogramacion.es)

---

## 🔝 HASHTAGS RECOMENDADOS PARA LINKEDIN

```
#React #TypeScript #Vite #TailwindCSS #WebDevelopment #Frontend 
#PersonalFinance #BudgetApp #JavaScript #ResponsiveDesign 
#ModernWeb #PCProgramacion #FinTech #WebApp #OpenSource 
#DeveloperPortfolio #ReactHooks #ContextAPI #LocalStorage 
#UserExperience #CleanCode #SoftwareDevelopment #TechInnovation
```

---

### 📅 **Información del Proyecto**
- **Año**: 2025
- **Versión**: 1.0.0
- **Última actualización**: Enero 2025
- **Estado**: ✅ Activo y en desarrollo
- **Licencia**: Propietaria - PCProgramación

---

<div align="center">

**🚀 ¿Listo para tomar control de tus finanzas?**

[📧 Contactar](mailto:desarrollo@pcprogramacion.es) • [🌐 Sitio Web](https://www.pcprogramacion.es) • [💼 LinkedIn](https://linkedin.com/in/francisco-jose-herreros)

**Desarrollado con ❤️ por [PCProgramación](https://www.pcprogramacion.es)**

</div>