# kttkpm-lab-6-docker
1. `docker --version`: Hiển thị version của docker trên thiết bị
![img_1.png](Evidences/img_docker_version.png)
2. `docker run hello-world`: Docker chạy image hello-world - image build sẵn của docker, nếu chưa có thì docker sẽ pull từ thư viện về 
![img.png](Evidences/img_docker_hello-world.png)
3. `docker pull nginx`: pull image nginx về local
![img.png](Evidences/img_docker_nginx.png)
4. `docker images`: Hiển thị tất cả các images đang có
![img.png](Evidences/img_docker_images.png)
5. `docker run -d nginx`: Chạy image nginx với flag `-d` hay `--detach` để chạy ngầm image nginx
![img.png](Evidences/img_docker_run_nginx.png)
6. `docker ps`: List các containers
![img.png](Evidences/img_docker_ps.png)
7. `docker ps -a`: List tất cả containers bao gồm các containers đã exited
![img.png](Evidences/img_docker_ps_a.png)
8. `docker logs <container_id>`: hiển thị logs của container chỉ định (f80:nginx)
![img.png](Evidences/img_docker_logs.png)
9. `docker exec -it <container_id> /bin/sh`: thực thi lệnh đối với container đang chạy. Ở đây chạy /bin/sh tức truy cập vào shell của container
![img.png](Evidences/img_docker_exec_sh.png)
10. `docker stop <container_id>`: Dừng container đang chạy
![img.png](Evidences/img_docker_stop.png)
11. `docker restart <container_id>`: Khởi dđộng lại container
![img.png](Evidences/img_docker_restart.png)
12. `docker rm <container_id>`: Xóa container với container id
![img_1.png](Evidences/img_docker_rm.png)
13. `docker container prune`: Xóa tất cả các containers đang stop
![img.png](Evidences/img_docker_container_prune.png)
14. `docker rmi <image_id>`: xóa Image với image id
![img.png](Evidences/img_docker_image_rmi.png)
15. `docker image prune -a`: Xoá tất cả image không hoạt động
![img.png](Evidences/img_docker_image_prune.png)
16. `docker run -d -p 8080:80 nginx`: khởi chaạy nginx với flag `-p` để map port <local port:docker container port>, tức map port 8080 ở máy local đến port 80 của host đang chạy nginx
![img.png](Evidences/img_docker_run_nginx_detach_port.png)
17. `docker inspect <container_id>`: Cung cấp thông tin chi tiết về cấu trúc container được kiểm soát bởi Docker thể hiện dưới JSON format. Gồm một số thông tin như: port binding, volume size, network, ip, state,...
![img.png](Evidences/img_docker_inspect_container.png)
18. `docker run -d -v mydata:/data nginx`: Chạy con nginx gắn volume tên mydata vào đường dẫn /data trong container. Nếu mydata chưa có sẽ tự tạo. Dữ liệu trong data sẽ lưu vào mydata nếu có xóa container đi thì vẫn không mất dữ liệu
![img.png](Evidences/img_docker_run_nginx_volume.png)
19. `docker volume ls`: list các volume
![img.png](Evidences/img_docker_volume_list.png)
20. `docker volume prune`: xóa tất cả các volume không được sử dụng bởi container nào
![img.png](Evidences/img_docker_volume_prune.png)
21. `docker -d --name my_nginx nginx`: Chạy con nginx và flag `--name` đăt tên cho container đó là my_nginx
![img.png](Evidences/img_docker_run_nginx_name.png)
22. `docker stats`: hiển thị trực tiếp resources mà container sử dụng như Task manager trên Windows hay `htop` trên linux
![img.png](Evidences/img_docker_stats.png)
23. `docker network ls`: liệt kê các network có trong docker. Caác cột: Network ID, Name, Driver, Scope. Network ID: id của mạng; Name: tên của network; Driver: loại driver dđể quản lý network gồm: Brigde, Host, None; Scope: Phạm vi của network
![img.png](Evidences/img_docker_network_list.png)
24. `docker network create my_network`: tạo network mới có tên là my_network
![img.png](Evidences/img_docker_network_create.png)
25. `docker run -d --network my_network --name my_container nginx`: Chạy con nginx với network là my_network và container tên my_container
![img.png](Evidences/img_docker_run_nginx_network.png)
26. `docker network connect my_network my_nginx`: Kết nóối container vào 1 network. Keết nối container my_nginx vào network my_network
![img.png](Evidences/img_docker_connect_network.png)
27. `docker run -d -e MY_ENV=hello_world nginx`: Chạy con nginx vóới thiết lập biến môi trường MY_ENV là Hello world
![img.png](Evidences/img_docker_run_nginx_env.png)
28. `docker logs -f my_nginx`: mở log của container teên my_nginx. Flag `-f` mở theo real-times
![img.png](Evidences/img_docker_logs_f.png)
29. create Dockerfile and basic index.html
![img.png](Evidences/img_create_Dockerfile.png)
30. `docker build -t my_nginx_image .`: Build file Dockerfile 
![img.png](Evidences/img_Docker_build_Dockerfile.png)
31. `docker run -d -p 8080:80 my_nginx_image`: run con my_nginx_image với port local 8080
![img.png](Evidences/img_docker_run_nginx_my_nginx_image.png)
![img.png](img.png)