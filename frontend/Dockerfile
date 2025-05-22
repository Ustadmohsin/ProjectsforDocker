FROM node:20

WORKDIR /app

COPY package*.json ./
RUN npm ci --prefer-offline

COPY . .

RUN npm run build

RUN npm install -g serve

EXPOSE 5173
CMD ["serve", "-l", "5173", "-s", "dist"]