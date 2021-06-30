FROM node:14.16.1-alpine3.13
WORKDIR /app
# Primeiro copia as dependências para aproveitar o cache de camadas
COPY package*.json ./ 
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "index.js"]