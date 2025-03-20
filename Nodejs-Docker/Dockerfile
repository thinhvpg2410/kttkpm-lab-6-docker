# sử dụng image node.js
FROM node:18
# thiết lập thư mục làm việc trong container
WORKDIR /app
# copy file package json vào thư muục làm việc
COPY package*.json ./
# install các dependencies
RUN npm install
#copy source code hiện tại vào container
COPY . .
#mở port 3000
EXPOSE 3000

CMD ["node", "hello-docker.js"]