FROM node:16

# Устанавливаем http-server
RUN npm install -g http-server

# Рабочая директория внутри контейнера
WORKDIR /app

# Указываем официальный npm реестр, чтобы не лез в taobao
RUN npm config set registry https://registry.npmjs.org

# Копируем package.json и package-lock.json (если есть)
COPY package*.json ./

# Устанавливаем зависимости с обходом конфликтов
RUN npm install --legacy-peer-deps

# Копируем весь код
COPY . .

# Собираем Vue приложение
RUN npm run build

# Запускаем http-сервер на 0.0.0.0 (чтобы доступ был извне контейнера)
CMD ["http-server", "dist", "-p", "8080", "-a", "0.0.0.0"]
