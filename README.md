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
