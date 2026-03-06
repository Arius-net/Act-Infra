# Usamos una versión ligera de Node
FROM node:18-alpine

# Directorio de trabajo dentro del contenedor
WORKDIR /usr/src/app

# Copiamos primero los archivos de dependencias para aprovechar la caché de Docker
COPY package*.json ./

# Instalamos las dependencias
RUN npm install

# Copiamos el resto del código fuente de tu API REST
COPY . .

# (Opcional) Si usas TypeScript y necesitas compilar el backend, descomenta la siguiente línea:
# RUN npm run build

# Exponemos el puerto de tu API
EXPOSE 3001

# Comando para arrancar el servidor (ajusta "start" por "dev" si usas nodemon)
CMD ["npm", "start"]