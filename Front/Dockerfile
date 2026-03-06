# Usamos una versión ligera de Node
FROM node:18-alpine

# Directorio de trabajo
WORKDIR /app

# Copiamos dependencias
COPY package*.json ./

# Instalamos las dependencias
RUN npm install

# Copiamos todo tu diseño, componentes y vistas
COPY . .

# Construimos la aplicación de Next.js para producción
RUN npm run build

# Exponemos el puerto que usa Next.js por defecto
EXPOSE 3000

# Arrancamos Next.js en modo producción
CMD ["npm", "start"]