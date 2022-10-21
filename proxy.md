Npm代理管理 （当将镜像从企业换到淘宝镜像时：查看代理 => 取消代理(如果有) => npm更换为淘宝镜像）

- 查看代理

  - npm config get proxy
  - npm config get https-proxy

- 配置代理

  - HTTP代理设置 (比如使用企业的代理，对应的代理链接公司提供)
    - npm config set proxy http://127.0.0.1:xxxx
    - npm config set https-proxy http://127.0.0.1:xxxx

  - SOCKS5 代理设置
    - git set http_proxy=socks5://127.0.0.1:1080
    - git set https_proxy=socks5://127.0.0.1:1080

- 取消代理
  - npm set http_proxy=
  - npm set https_proxy=
  - git config --global --unset http.proxy
  - git config --global --unset https.proxy

- Npm 更换为淘宝镜像源

  - 单次使用 npm install --registry=https://registry.npm.taobao.org

  - 永久使用 npm config set registry https://registry.npm.taobao.org

  - 检查是否设置成功  

    ```
    npm config get registry
    // 或
    npm info express
    ```

![image-20210306012525516](/Users/mac/Documents/project/notes/images/proxy.png)
