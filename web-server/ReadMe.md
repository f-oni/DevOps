# Setting up a Web Server

## Introdction
A project to set up web servr using `Docker` and `Nginx`. The project introduces a fictitius cafe website with the name `Erudite Cafe`. 

## Project Steps

1 **Project Directory:** A project directory was created with the name `cafe-app`. A sub-directory with the name `Erudite_cafe` was created to contain all the website files

 <img width="802" height="285" alt="proj-files" src="https://github.com/user-attachments/assets/3a8c03e7-ba72-4e6e-be7a-b629329b73a8" />
 

 <img width="1177" height="628" alt="proj-files-2" src="https://github.com/user-attachments/assets/bfe6183c-79ef-44ef-86cb-8703c757d880" />


2. **Dockerfile:** A docker file was created with the following content

   ```
    FROM nginx:alpine
    COPY Erudite_cafe /usr/share/nginx/html
    EXPOSE 80
   
   ```
3. **Image:** An image was built from the `Dockerfile` with the command `docker build . -t folu980/cafe-app:0.1.` The image was successfully built as shown below:

    <img width="1487" height="461" alt="docker-1" src="https://github.com/user-attachments/assets/c97e75d2-f6ad-4944-81cd-097f82398435" />

    <img width="959" height="297" alt="img" src="https://github.com/user-attachments/assets/0cf86378-5f2b-4b67-abaa-c35861313404" />


4. **Container** A container was started with the command `docker run -d --name cafe-app -p 4040:80 folu980/cafe-app:0.1`. Port 80 of the container was mapped to 4040 of the localhost

   <img width="1409" height="288" alt="docker-2" src="https://github.com/user-attachments/assets/34d195cc-cf71-4d7c-b7f3-510f243c7c48" />

5. **Validation** The website was accessed locally from the browser by navigating to `http://localhost:4040`

   <img width="1635" height="943" alt="browser" src="https://github.com/user-attachments/assets/4550f1bc-d29c-40f9-95f7-330ced4a1e41" />


## Conclusion

A docker container was created to run a web server
