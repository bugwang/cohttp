# cohttp
The goal is to hunt and kill the microservices of go.

idea：
http server api ，http client api:
use epoll 
use pool
use coroutine
and Don't depend on third party or only header file
but i need time

desc：

        server
        one loop per pthread  - > co_pool per loop -> ( one request one co)  for  parallel hander

        hander
        a or s io for (one request -> more demand -> parallel demand per co -> one reply)

step 1. no coroutine

<img width="659" height="130" alt="图片" src="https://github.com/user-attachments/assets/bc6081e6-02e0-42fd-a710-37940f1bd219" />

<img width="659" height="132" alt="图片" src="https://github.com/user-attachments/assets/d0912744-bb77-4fd7-b6f6-1387f4dff55e" />
