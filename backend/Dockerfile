# Etapa 1: Usar a imagem base do Node.js
FROM node:14

# Etapa 2: Definir o diretório de trabalho no container
WORKDIR /app

# Etapa 3: Copiar o package.json e package-lock.json
COPY package*.json ./

# Etapa 4: Instalar as dependências do back-end
RUN npm install

# Etapa 5: Copiar o restante dos arquivos da aplicação para o container
COPY . .

# Etapa 6: Expor a porta 5000 (padrão do Express)
EXPOSE 5000

# Etapa 7: Comando para rodar a aplicação Node.js
CMD ["npm", "start"]
