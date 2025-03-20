# sử dụng image python 3.9
FROM python:3.9
# thiết lập thư mục làm việc trong container
WORKDIR /app
# copy file requirements vào 
COPY requirements.txt requirements.txt
#cài đặt các thư viện treong requirements
RUN pip install --no-cache-dir -r requirements.txt
# copy source code vào container
COPY . .
# mở port 5000
EXPOSE 5000

CMD ["python", "app.py"]