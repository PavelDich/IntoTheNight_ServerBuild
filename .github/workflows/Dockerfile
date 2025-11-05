FROM ubuntu:20.04

# Установка зависимостей для Unity
RUN apt-get update && apt-get install -y \
    libssl1.1 \
    libx11-6 \
    libxrandr2 \
    libxcursor1 \
    libxinerama1 \
    libxi6 \
    libgl1-mesa-glx \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

# Копирование билда Unity
COPY Build/Linux/ ./

# Даем права на исполнение
RUN chmod +x ./GF_server.x86_64

EXPOSE 2706

CMD ["./GF_server.x86_64"]