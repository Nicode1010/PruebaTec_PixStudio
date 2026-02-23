# 🚀 PIX RPA – Prueba Técnica Desarrollador RPA

Automatización desarrollada en **PIX Robotics Studio**, que simula un flujo empresarial completo de monitoreo de productos eCommerce, almacenamiento estructurado, generación de reportes y envío automatizado mediante formulario web.

---

## 🎯 Objetivo General

Desarrollar un proceso RPA utilizando la plantilla universal de PIX RPA que integre:

- Consumo de API REST
- Persistencia en base de datos
- Generación automatizada de reportes
- Automatización web (formulario con adjunto)

---

## 🏢 Contexto del Caso

Una empresa ficticia de análisis de comercio electrónico desea automatizar el proceso de:

1. Descarga de productos desde una tienda online.
2. Registro estructurado en base de datos.
3. Generación de reportes ejecutivos.
4. Envío automatizado del informe vía formulario web interno.

---

# ⚙️ Flujo del Proceso

## 1️⃣ Consumo de API Pública

- **Endpoint:** https://fakestoreapi.com/products
- Método: `GET`
- Respuesta almacenada como respaldo en:

```
Data/Input/data.json
```

Campos extraídos:

- `id`
- `title`
- `price`
- `category`
- `description`

---

## 2️⃣ Inserción en Base de Datos

Los productos son almacenados en la tabla `Productos` con los siguientes campos:

- id  
- title  
- price  
- category  
- description  
- fecha_insercion  

Se valida previamente la existencia de registros para evitar duplicidad.

---

## 3️⃣ Generación de Reporte en Excel

Se genera un archivo Excel en:

```
Data/Reportes/
```

El reporte contiene:

### 📄 Hoja 1 – Listado completo
- Todos los productos descargados

### 📊 Hoja 2 – Métricas resumen
- Cantidad total de productos
- Precio promedio general
- Precio promedio por categoría
- Cantidad de productos por categoría

---

## 4️⃣ Automatización Web – Envío de Formulario

- **URL:**  
  https://form.jotform.com/260496498158069

Campos automatizados:

- Nombre colaborador  
- Fecha de reporte  
- Comentarios  
- Adjuntar archivo Excel generado  

Se genera evidencia de ejecución en:

```
Data/Output/
```

Incluye captura `.png` del envío exitoso.

---


---

# 🛠️ Configuración y Ejecución

## 1️⃣ Clonar repositorio

```bash
git clone https://github.com/Nicode1010/PruebaTec_PixStudio.git
```

O descargar manualmente el repositorio.

---

## 2️⃣ Configuración

Editar el archivo:

```
Data/Config.xlsx
```

Configurar:

- URL de la API  
- Parámetros de base de datos  
- Rutas locales  
- Datos del formulario  

> ⚠ IMPORTANTE  
> El bot fue desarrollado para trabajar con **SQL Server**.  
> Ajustar host, puerto, usuario y contraseña según el entorno.

---

## 3️⃣ Ejecución

1. Abrir el archivo `.pixproj` en PIX Studio  
2. Ejecutar el proceso principal  
3. Verificar generación de:

- JSON de respaldo  
- Inserción en BD  
- Archivo Excel  
- Envío automático del formulario  

---

# 📌 Resultados Esperados

✔ Archivo JSON generado  
✔ Registros almacenados en base de datos  
✔ Excel con métricas consolidadas  
✔ Formulario enviado automáticamente  
✔ Evidencia de ejecución generada  

---

# 🎥 Video Demostración

El video demostrativo del funcionamiento del proceso fue enviado adjunto al correo correspondiente.
