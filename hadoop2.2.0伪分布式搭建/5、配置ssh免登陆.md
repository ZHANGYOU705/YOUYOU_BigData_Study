## 配置ssh免密登陆

* 生成ssh免登陆密钥


       cd ~，进入到我的home目录
       cd .ssh/

       ssh-keygen -t rsa （四个回车）
    

  * 执行完这个命令后，会生成两个文件id_rsa（私钥）、id_rsa.pub（公钥）
  * 将公钥拷贝到要免登陆的机器上
  
            cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
            或
            ssh-copy-id -i localhost 
## ssh免密登陆原理
![ssh免登陆原理](../img/ssh免登陆原理.png)
