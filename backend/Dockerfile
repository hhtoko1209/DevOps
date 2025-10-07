# Dựa trên Node 20 Alpine — nhẹ và nhanh
FROM node:20-alpine

# Tạo thư mục làm việc
WORKDIR /app

# Copy package info trước để tận dụng cache
COPY package*.json ./

# Cài dependencies (nếu có package-lock.json thì dùng npm ci)
# Nếu chưa có lockfile thì dùng npm install
RUN if [ -f package-lock.json ]; then npm ci --omit=dev; else npm install --omit=dev; fi

# Copy toàn bộ mã nguồn
COPY . .

# Mở cổng server (nếu bạn dùng cổng khác, đổi ở đây)
EXPOSE 3000

# Lệnh khởi chạy ứng dụng
CMD ["npm", "start"]
