# Sử dụng Node 18 Alpine
FROM node:18-alpine

# Tạo thư mục làm việc trong container
WORKDIR /app

# Sao chép file package.json và package-lock.json trước
COPY package*.json ./

# Cài đặt dependencies
RUN npm install

# Sao chép toàn bộ mã nguồn vào container
COPY . .

# Expose cổng 5000 (hoặc port app bạn đang dùng)
EXPOSE 5000

# Lệnh khởi chạy ứng dụng
CMD ["npm", "start"]
