# Flask Product API

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-2.0%2B-green.svg)](https://flask.palletsprojects.com/)
[![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-1.4%2B-orange.svg)](https://www.sqlalchemy.org/)
[![Marshmallow](https://img.shields.io/badge/Marshmallow-3.0%2B-yellow.svg)](https://marshmallow.readthedocs.io/)
[![License](https://img.shields.io/badge/License-MIT-red.svg)](https://opensource.org/licenses/MIT)

Una API RESTful para gestionar productos, construida con Flask y SQLAlchemy. Esta aplicación proporciona endpoints para realizar operaciones CRUD completas sobre productos.

## Características

- ✅ Operaciones CRUD completas
- ✅ Validación de datos con Marshmallow
- ✅ Base de datos SQL con SQLAlchemy
- ✅ Migraciones de base de datos con Flask-Migrate
- ✅ Documentación de API con ejemplos
- ✅ Manejo de errores robusto

## Requisitos Previos

- Python 3.8 o superior
- pip (gestor de paquetes de Python)
- Git (opcional, para clonar el repositorio)

## Instalación en Ubuntu

1. **Instalar Python y pip (si no están instalados):**
   ```bash
   sudo apt update
   sudo apt install python3 python3-pip python3-venv
   ```

2. **Clonar el repositorio (opcional):**
   ```bash
   git clone <url-del-repositorio>
   cd backend.flask
   ```

3. **Crear y activar el entorno virtual:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

4. **Instalar dependencias:**
   ```bash
   pip install -r requirements.txt
   ```

## Configuración

1. **Configurar variables de entorno:**
   ```bash
   export FLASK_APP=app.py
   export FLASK_ENV=development
   ```

2. **Inicializar la base de datos:**
   ```bash
   flask db init
   flask db migrate -m "Initial migration"
   flask db upgrade
   ```

## Ejecución

Para iniciar la aplicación:

```bash
python app.py
```

La aplicación estará disponible en `http://localhost:3000`

## Endpoints de la API

### Obtener todos los productos
```bash
GET /api/products
```

### Obtener un producto específico
```bash
GET /api/products/{id}
```

### Crear un nuevo producto
```bash
POST /api/products
Content-Type: application/json

{
    "name": "Producto Ejemplo",
    "price": 99.99,
    "description": "Descripción del producto"
}
```

### Actualizar un producto
```bash
PUT /api/products/{id}
Content-Type: application/json

{
    "name": "Producto Actualizado",
    "price": 149.99,
    "description": "Nueva descripción"
}
```

### Eliminar un producto
```bash
DELETE /api/products/{id}
```

## Ejemplos de Uso con curl

### Crear un producto
```bash
curl -X POST http://localhost:3000/api/products \
  -H "Content-Type: application/json" \
  -d '{"name": "Laptop Gaming", "price": 1299.99, "description": "Laptop gaming de alta gama"}'
```

### Obtener todos los productos
```bash
curl http://localhost:3000/api/products
```

## Estructura del Proyecto

```
backend.flask/
├── app.py              # Aplicación principal
├── config.py           # Configuración
├── models.py           # Modelos de la base de datos
├── schemas.py          # Esquemas de validación
├── requirements.txt    # Dependencias
└── README.md          # Documentación
```

## Contribución

1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

