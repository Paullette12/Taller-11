
# Imagen base: Node.js 26 sobre Alpine Linux.
FROM node:26-alpine

# Carpeta de trabajo dentro de la imagen.
WORKDIR /app

# Copiar archivos de dependencias.
COPY package*.json ./
RUN npm ci --omit=dev --ignore-scripts

# Copiar el resto del código.
COPY . .

# Ejecutar con un usuario sin privilegios.
USER node

# Puerto del servidor.
EXPOSE 3000

# Comando de inicio.
CMD ["node", "servidor.js"]
